---
description: VSDiagview e VSSAgent sono strumenti che è possibile usare per risolvere i problemi relativi alle applicazioni VSS. Si noti che questi strumenti sono inclusi in Microsoft Windows Software Development Kit (SDK) per Windows Vista e versioni successive.
ms.assetid: 2c1270a6-38c7-40d5-a194-0a6795557b9f
title: Uso della diagnostica VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3d1733c2780670507b39c1db91cb3b2f7035a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307180"
---
# <a name="using-vss-diagnostics"></a>Uso della diagnostica VSS

VSDiagview e VSSAgent sono strumenti che è possibile usare per risolvere i problemi relativi alle applicazioni VSS.

> [!Note]  
> Questi strumenti sono inclusi in Microsoft Windows Software Development Kit (SDK) per Windows Vista e versioni successive. È possibile scaricare il Windows SDK da [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .

 

Nell'installazione di Windows SDK, questi strumenti sono disponibili in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (per Windows a 64 bit) e `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (per windows a 32 bit).

## <a name="gathering-data"></a>Raccolta dati

È possibile raccogliere dati tramite il comando VSSAgent.

**Per raccogliere dati mediante VSSAgent**

1.  Per raccogliere dati dalla riga di comando, usare il comando VSSAgent come segue:

    **VSSAgent-raccoglie** *xmlFileName * * *. XML**

2.  Per visualizzare il file di output, vedere la sezione seguente relativa alla visualizzazione dei dati.

## <a name="viewing-data"></a>Visualizzazione dei dati

L'applicazione VSDiagview può essere usata per visualizzare i dati raccolti tramite il comando VSSAgent. VSDiagview Visualizza le informazioni seguenti sul computer:

-   Informazioni sul computer, ad esempio la versione del sistema operativo, la memoria totale disponibile e la velocità della CPU
-   I nomi e i numeri di versione dei file binari VSS
-   I nomi e le proprietà dei dispositivi disco e volume
-   I nomi e le proprietà di qualsiasi applicazione COM+
-   Nomi dei registri eventi che possono essere utilizzati per la diagnosi dei problemi del servizio Copia Shadow del volume
-   I nomi dei writer VSS e degli eventi gestiti
-   Informazioni su altri file del sistema operativo

**Per visualizzare i dati tramite VSDiagview**

1.  Scegliere **Apri** dal menu file per cercare un file. (Il percorso predefinito è C: \\ vssdiag).
2.  Fare clic su **Apri** per visualizzare i dati.

 

 



