---
description: Per semplificare l'implementazione del driver quanto più possibile, Windows Image Acquisition (WIA) fornisce una libreria di servizi minidriver che esegue molte delle attività amministrative richieste dall'architettura WIA.
ms.assetid: 074a53a3-20b0-4b25-991d-5d48f75c5d75
title: Libreria di servizi WIA minidriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45856fb795810e4e447a226f1b92a28698f08cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307311"
---
# <a name="wia-minidriver-service-library"></a>Libreria di servizi WIA minidriver

Per semplificare l'implementazione del driver quanto più possibile, Windows Image Acquisition (WIA) fornisce una libreria di servizi minidriver che esegue molte delle attività amministrative richieste dall'architettura WIA. La libreria del servizio fornisce funzioni di supporto per la gestione dell'albero del dispositivo degli oggetti dell' [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) .

Le funzioni di base della libreria di servizi eseguono le funzioni di supporto che la maggior parte dei driver di dispositivo avrebbe altrimenti necessario implementare. Queste funzioni leggono e scrivono le proprietà. Creano inoltre oggetti elemento del driver e copia le proprietà delle informazioni sul dispositivo.

 

 



