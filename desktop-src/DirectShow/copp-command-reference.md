---
description: Informazioni di riferimento sul comando COPP
ms.assetid: b21db1cf-cac3-41d6-8189-6e01c8f91a7d
title: Informazioni di riferimento sul comando COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1a706863464b6f303e05cb88e28a075dffbfba7b6bf54f8289a2699e66a76f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565971"
---
# <a name="copp-command-reference"></a>Informazioni di riferimento sul comando COPP

In questa sezione vengono descritti i comandi COPP (Certified Output Protection Protocol). Vengono definiti i comandi seguenti.



| Comando              | GUID                             |
|----------------------|----------------------------------|
| Impostare il livello di protezione | **DXVA \_ COPPSetProtectionLevel** |
| Impostare la segnalazione        | **DXVA \_ COPPSetSignaling**       |



 

Comando Imposta livello di protezione

Imposta il livello di protezione per un meccanismo di protezione dell'output specificato. A seconda del connettore, potrebbe essere possibile applicare più meccanismi di protezione sullo stesso connettore, con impostazioni diverse per ogni meccanismo.

**GUID:** DXVA \_ COPPSetProtectionLevel

**Dati di input:** [**struttura \_ DXVA COPPSetProtectionLevelCmdData.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata)

Impostare il comando di segnalazione

Specifica informazioni sul segnale video diverso dal livello di protezione.

Per CGMS-A, alcuni standard di protezione richiedono che il segnale di televsion contenga informazioni sulle proporzioni e altre informazioni all'interno degli stessi pacchetti di forma d'onda VBI dei bit CGMS-A. Se le informazioni sulle proporzioni non sono coerenti con il flusso video, è possibile che i programmi televisivi non siano visualizzati in modo non coerente. L'applicazione può usare questo comando per specificare le proporzioni in modo che il driver di grafica possa generare i pacchetti VBI corretti.

Questo comando è progettato anche per essere estendibile se sono necessarie informazioni aggiuntive sui segnali negli standard futuri.

**GUID:** DXVA \_ COPPSetSignaling

**Dati di input:** [**struttura \_ DXVA COPPSetSignalingCmdData.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del protocollo COPP (Certified Output Protection Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



