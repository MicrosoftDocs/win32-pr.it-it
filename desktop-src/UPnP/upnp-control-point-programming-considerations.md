---
title: Considerazioni sulla programmazione del punto di controllo
description: Gli sviluppatori che creano applicazioni basate su UPnP (o punti di controllo) devono usare queste applicazioni da un \_ client ApartmentThreaded di CoInit. Si sono verificati problemi noti quando si usa l'API del punto di controllo da un \_ client multithread CoInit eseguito in condizioni di stress.
ms.assetid: a5d79a29-4192-40af-b75d-a31f1f46149c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76955177f9fc0c3b164d84998547c1afdfbfb4bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856665"
---
# <a name="control-point-programming-considerations"></a>Considerazioni sulla programmazione del punto di controllo

Gli sviluppatori che creano applicazioni basate su UPnP (o punti di controllo) devono usare queste applicazioni da un \_ client ApartmentThreaded di CoInit. Si sono verificati problemi noti quando si usa l'API del punto di controllo da un \_ client multithread CoInit eseguito in condizioni di stress.

 

 




