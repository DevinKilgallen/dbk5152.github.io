import { Card, CardContent, CardHeader, CardTitle } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Progress } from "@/components/ui/progress";
import { Dumbbell, Flame, Clock, Trophy } from "lucide-react";
import { motion } from "framer-motion";

export default function FitnessAppHome() {
  return (
    <div className="min-h-screen bg-gray-100 p-6 flex flex-col gap-6">
      {/* Header */}
      <motion.header
        initial={{ opacity: 0, y: -20 }}
        animate={{ opacity: 1, y: 0 }}
        className="flex justify-between items-center"
      >
        <h1 className="text-2xl font-bold text-gray-800">Welcome Back, Athlete!</h1>
        <Button variant="outline">Profile</Button>
      </motion.header>

      {/* Daily Stats */}
      <motion.section
        initial={{ opacity: 0, y: 20 }}
        animate={{ opacity: 1, y: 0 }}
        className="grid grid-cols-2 md:grid-cols-4 gap-4"
      >
        <Card>
          <CardHeader className="flex items-center gap-2">
            <Flame className="text-orange-500" />
            <CardTitle>Calories</CardTitle>
          </CardHeader>
          <CardContent>
            <p className="text-2xl font-semibold">1,250 kcal</p>
            <Progress value={62} className="mt-2" />
          </CardContent>
        </Card>

        <Card>
          <CardHeader className="flex items-center gap-2">
            <Clock className="text-blue-500" />
            <CardTitle>Workout Time</CardTitle>
          </CardHeader>
          <CardContent>
            <p className="text-2xl font-semibold">45 min</p>
            <Progress value={75} className="mt-2" />
          </CardContent>
        </Card>

        <Card>
          <CardHeader className="flex items-center gap-2">
            <Dumbbell className="text-green-500" />
            <CardTitle>Exercises</CardTitle>
          </CardHeader>
          <CardContent>
            <p className="text-2xl font-semibold">8 done</p>
            <Progress value={80} className="mt-2" />
          </CardContent>
        </Card>

        <Card>
          <CardHeader className="flex items-center gap-2">
            <Trophy className="text-yellow-500" />
            <CardTitle>Streak</CardTitle>
          </CardHeader>
          <CardContent>
            <p className="text-2xl font-semibold">5 days</p>
            <Progress value={50} className="mt-2" />
          </CardContent>
        </Card>
      </motion.section>

      {/* Quick Actions */}
      <motion.section
        initial={{ opacity: 0, y: 20 }}
        animate={{ opacity: 1, y: 0 }}
        className="grid grid-cols-1 md:grid-cols-3 gap-4"
      >
        <Card className="text-center p-6">
          <CardHeader>
            <CardTitle>Start Workout</CardTitle>
          </CardHeader>
          <CardContent>
            <Button className="w-full bg-green-600 hover:bg-green-700 text-white">Go</Button>
          </CardContent>
        </Card>

        <Card className="text-center p-6">
          <CardHeader>
            <CardTitle>View Progress</CardTitle>
          </CardHeader>
          <CardContent>
            <Button className="w-full bg-blue-600 hover:bg-blue-700 text-white">Open</Button>
          </CardContent>
        </Card>

        <Card className="text-center p-6">
          <CardHeader>
            <CardTitle>Nutrition Tracker</CardTitle>
          </CardHeader>
          <CardContent>
            <Button className="w-full bg-orange-600 hover:bg-orange-700 text-white">Track</Button>
          </CardContent>
        </Card>
      </motion.section>
    </div>
  );
}
