---
description: Per semplificare il più possibile l'implementazione dei driver, Windows Image Acquisition (WIA) fornisce una libreria del servizio Minidriver che esegue molte delle attività amministrative richieste dall'architettura WIA.
ms.assetid: 074a53a3-20b0-4b25-991d-5d48f75c5d75
title: Libreria del servizio WiA Minidriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0008e19fbbdb31000535fa10f34bfacebfd6c6180964fa3e3fb18502f22a28d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207931"
---
# <a name="wia-minidriver-service-library"></a>Libreria del servizio WiA Minidriver

Per semplificare il più possibile l'implementazione dei driver, Windows Image Acquisition (WIA) fornisce una libreria del servizio Minidriver che esegue molte delle attività amministrative richieste dall'architettura WIA. La libreria di servizi fornisce funzioni helper per gestire l'albero del dispositivo di [oggetti interfaccia IWiaDrvItem.](https://msdn.microsoft.com/library/ms793976.aspx)

Le funzioni della libreria di servizi di base eseguono funzioni helper che la maggior parte dei driver di dispositivo avrebbe altrimenti bisogno di implementare. Queste funzioni leggono e scrivono proprietà. Creano anche oggetti elemento driver e copiano le proprietà delle informazioni sul dispositivo.

 

 



