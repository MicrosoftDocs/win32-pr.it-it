---
description: MFTrace è uno strumento per la generazione di log di traccia per applicazioni Media Foundation.
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a216f225141ceccf3f1357025dd069afa494d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325218"
---
# <a name="mftrace"></a>MFTrace

MFTrace è uno strumento per la generazione di log di traccia per applicazioni Media Foundation.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Uso di MFTrace](using-mftrace.md)
-   [Parole chiave MFTrace](mftrace-keywords.md)
-   [File di configurazione MFTrace](mftrace-configuration-file.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|---------------------------------------------------------------------------------------|
| Versione minima dell'SDK      | Microsoft Windows Software Development Kit (SDK) per Windows 7 e .NET Framework 4,0 |
| Sistema operativo minimo | Windows Vista                                                                         |



 

MFTrace richiede le DLL seguenti, fornite anche nell'SDK.

-   detoured.dll
-   mfdetours.dll

L'SDK fornisce le versioni di MFTrace a 32 bit e a 64 bit. MFTrace non supporta WOW64; per tracciare un processo a 32 bit in esecuzione su Windows a 64 bit, usare la versione a 32 bit di MFTrace.

SDK-root nei sistemi a 32 bit: \Programmi\microsoft Kits\10 SDK-root in 64 bit System: \Program Files (x86) \Windows Kits\10 sono disponibili mftrace in <SDK-root> \bin \<sdk-version> \<architecture>\mftrace.exe

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strumenti di Media Foundation](media-foundation-tools.md)
</dt> </dl>

 

 



