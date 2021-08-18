---
description: Vsdiagview e Vssagent sono strumenti che è possibile usare per risolvere i problemi delle applicazioni VSS. Nota Questi strumenti sono inclusi in Microsoft Windows Software Development Kit (SDK) per Windows Vista e versioni successive.
ms.assetid: 2c1270a6-38c7-40d5-a194-0a6795557b9f
title: Uso della diagnostica vss
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7742bf706da0bb8fdd377960a597a61b6592b772df98982cec500434f66c7579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590804"
---
# <a name="using-vss-diagnostics"></a>Uso della diagnostica vss

Vsdiagview e Vssagent sono strumenti che è possibile usare per risolvere i problemi delle applicazioni VSS.

> [!Note]  
> Questi strumenti sono inclusi in Microsoft Windows Software Development Kit (SDK) per Windows Vista e versioni successive. È possibile scaricare l'SDK Windows da [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .

 

Nell'Windows SDK di Windows questi strumenti sono disponibili in (per il Windows a 64 bit) e (per le Windows `%Program Files(x86)%\Windows Kits\8.1\bin\x64` `%Program Files(x86)%\Windows Kits\8.1\bin\x86` a 32 bit).

## <a name="gathering-data"></a>Raccolta di dati

È possibile raccogliere dati usando il comando Vssagent.

**Per raccogliere dati tramite Vssagent**

1.  Per raccogliere dati dalla riga di comando, usare il comando Vssagent come indicato di seguito:

    **vssagent -gather** *XmlFileName***.xml**

2.  Per visualizzare il file di output, vedere la sezione Visualizzazione dei dati seguente.

## <a name="viewing-data"></a>Visualizzazione dei dati

L'applicazione Vsdiagview può essere usata per visualizzare i dati raccolti usando il comando Vssagent. Vsdiagview visualizza le informazioni seguenti sul computer:

-   Informazioni sul computer, ad esempio la versione del sistema operativo, la memoria totale disponibile e la velocità della CPU
-   Nomi e numeri di versione dei file binari vss
-   Nomi e proprietà dei dispositivi disco e volume
-   Nomi e proprietà di qualsiasi applicazione COM+
-   I nomi dei log eventi che possono essere usati per diagnosticare i problemi del Servizio Copia Studio
-   I nomi di qualsiasi vss writer e gli eventi che gestiscono
-   Informazioni su altri file del sistema operativo

**Per visualizzare i dati con Vsdiagview**

1.  Scegliere Apri dal menu File **per** cercare un file. Il percorso predefinito è C: \\ vssdiag.
2.  Fare **clic su** Apri per visualizzare i dati.

 

 



