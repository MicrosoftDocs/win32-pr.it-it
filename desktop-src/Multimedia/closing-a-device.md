---
title: Chiusura di un dispositivo
description: Chiusura di un dispositivo
ms.assetid: eef40f23-2c58-4deb-a6f0-3563d9c30d10
keywords:
- MCI_CLOSE comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f81ddaf42ef5509b55271159b8e36ac56584b92734a6b04e5b555041596530
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498081"
---
# <a name="closing-a-device"></a>Chiusura di un dispositivo

Il [**comando close**](close.md) ([**MCI \_ CLOSE**](mci-close.md)) rilascia l'accesso a un dispositivo o a un file. MCI libera un dispositivo quando tutte le attività che lo usano lo hanno chiuso. Per consentire a MCI di gestire i dispositivi, l'applicazione deve chiudere ogni dispositivo o file al termine dell'uso.

Quando si chiude un dispositivo MCI esterno che usa il proprio supporto anziché i file (ad esempio l'audio CD), il driver lascia il dispositivo nella modalità di funzionamento corrente. Pertanto, se si chiude un dispositivo audio CD in riproduzione, anche se il driver di dispositivo viene rilasciato dalla memoria, il dispositivo audio CD continuerà a essere riprodotto fino a quando non raggiungerà la fine del contenuto.

> [!Note]  
> La chiusura di un'applicazione con dispositivi MCI aperti può impedire ad altre applicazioni di usare tali dispositivi fino Windows riavvio.

 

 

 




