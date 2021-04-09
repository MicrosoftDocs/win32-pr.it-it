---
title: Alcuni pannelli di input software IME per l'Asia orientale inviano ora vKey
description: Alcuni pannelli di input software IME per l'Asia orientale inviano ora vKey
ms.assetid: 5E3BE112-D962-4C11-B31E-229584191FAE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c444091e4498582cccc4378dfa2f17216cbf810
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103857013"
---
# <a name="some-east-asian-ime-software-input-panels-now-send-vkey"></a>Alcuni pannelli di input software IME per l'Asia orientale inviano ora vKey

## <a name="platforms"></a>Piattaforme

<dl> Client-Windows 8.1  
Server-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrizione

In Windows 8, se è selezionato uno degli IME asiatici orientali, la pressione di una chiave del pannello di input software non ha inviato vo.

In Windows 8.1 vengono inviati vo per le configurazioni seguenti:



| Linguaggio            | IME                                 | Windows Store | Desktop |
|---------------------|-------------------------------------|---------------|---------|
| Cinese semplificato  | Microsoft Pinyin, Microsoft Wubi    | Sì           | Sì     |
| Cinese tradizionale | Microsoft Changlie, Microsoft Quick | Sì           | Sì     |
| Cinese tradizionale | Microsoft Bopomofo                  | No            | No      |
| Coreano              | Microsoft IME                       | Sì           | No      |
| Giapponese            | Microsoft IME                       | No            | No      |



 

## <a name="manifestations"></a>Manifestazioni

Se l'utente sceglie un IME che non invia vo, le funzioni attivate da vKey non funzionano.

## <a name="solution"></a>Soluzione

Le applicazioni che non utilizzano una delle configurazioni IME indicate in precedenza devono essere progettate in modo da consentire agli utenti di completare l'attività desiderata senza utilizzare le funzioni che richiedono vo.

Se l'utente sceglie un IME che invia vo, ma l'applicazione è stata progettata senza tale previsione, l'applicazione deve essere modificata per riconoscere quale versione di Windows è in esecuzione e rispondere di conseguenza.

 

 




