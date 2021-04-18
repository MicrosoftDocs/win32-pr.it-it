---
description: Riferimento al comando COPP
ms.assetid: b21db1cf-cac3-41d6-8189-6e01c8f91a7d
title: Riferimento al comando COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50dfeebe42b877604ab880ef1855035242d6eca8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304328"
---
# <a name="copp-command-reference"></a>Riferimento al comando COPP

In questa sezione vengono descritti i comandi COPP (Certified Output Protocol). Vengono definiti i comandi seguenti.



| Comando              | GUID                             |
|----------------------|----------------------------------|
| Imposta il livello di protezione | **\_COPPSETPROTECTIONLEVEL DXVA** |
| Imposta segnalazione        | **\_COPPSETSIGNALING DXVA**       |



 

Comando Imposta livello di protezione

Imposta il livello di protezione per un meccanismo di protezione dell'output specificato. A seconda del connettore, potrebbe essere possibile applicare più di un meccanismo di protezione sullo stesso connettore, con impostazioni diverse per ogni meccanismo.

**GUID**: DXVA \_ COPPSetProtectionLevel

**Dati di input**: [**struttura \_ COPPSetProtectionLevelCmdData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) .

Imposta comando di segnalazione

Specifica informazioni sul segnale video diverso dal livello di protezione.

Per CGMS-A, determinati standard di protezione richiedono che il segnale Televsion contenga informazioni sulle proporzioni e altre informazioni all'interno degli stessi pacchetti di forme d'onda VBI dei bit CGMS-A. I televisori potrebbero non essere visualizzati correttamente se le informazioni sulle proporzioni non sono coerenti con il flusso video. L'applicazione può utilizzare questo comando per specificare le proporzioni in modo che il driver di grafica possa generare i pacchetti VBI corretti.

Questo comando è anche progettato per essere estendibile se sono necessarie informazioni aggiuntive sul segnale negli standard futuri.

**GUID**: DXVA \_ COPPSetSignaling

**Dati di input**: [**struttura \_ COPPSetSignalingCmdData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di COPP (Certified Output Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



