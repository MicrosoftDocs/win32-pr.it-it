---
description: MFTrace è uno strumento per la generazione di log di traccia per Media Foundation applicazioni.
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542ac9325b33fc8f1a76394d203dbf1d27919bd6
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885225"
---
# <a name="mftrace"></a>MFTrace

MFTrace è uno strumento per la generazione di log di traccia per Media Foundation applicazioni.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Uso di MFTrace](using-mftrace.md)
-   [Parole chiave di MFTrace](mftrace-keywords.md)
-   [File di configurazione di MFTrace](mftrace-configuration-file.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|---------------------------------------------------------------------------------------|
| Versione minima dell'SDK      | Microsoft Windows Software Development Kit (SDK) per Windows 7 e .NET Framework 4.0 |
| Sistema operativo minimo | Windows Vista                                                                         |



 

MFTrace richiede le DLL seguenti, disponibili anche nell'SDK.

-   detoured.dll
-   mfdetours.dll

L'SDK fornisce sia le versioni a 32 bit che a 64 bit di MFTrace. MFTrace non supporta WOW64; per tracciare un processo a 32 bit in esecuzione su Windows a 64 bit, usare la versione a 32 bit di MFTrace.

sdk-root nei sistemi a 32 bit: \Programmi\Windows Kits\10 sdk-root in un sistema a 64 bit: \Programmi (x86)\Windows Kits\10 È possibile trovare mftrace in &lt; sdk-root &gt; \bin \<sdk-version> \<architecture>\mftrace.exe

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation strumenti](media-foundation-tools.md)
</dt> </dl>

 

 



