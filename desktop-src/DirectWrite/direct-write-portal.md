---
title: DirectWrite (DWrite)
description: Le applicazioni attuali devono supportare il rendering di testo di alta qualità, i tipi di carattere di struttura indipendenti dalla risoluzione e il testo Unicode completo e il supporto del layout. DirectWrite, un'API [DirectX](../directx.md) , fornisce queste funzionalità e altro ancora.
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b1e2ff44083a56a7202847fc07ad9daaa67b7ba
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2020
ms.locfileid: "104475016"
---
# <a name="directwrite-dwrite"></a>DirectWrite (DWrite)

## <a name="purpose"></a>Scopo

Le applicazioni attuali devono supportare il rendering di testo di alta qualità, i tipi di carattere di struttura indipendenti dalla risoluzione e il testo Unicode completo e il supporto del layout. DirectWrite, un'API [DirectX](../directx.md) , fornisce queste funzionalità e altro ancora.

- Sistema di layout del testo indipendente dal dispositivo che migliora la leggibilità del testo nei documenti e nell'interfaccia utente.
- Rendering di testo di alta qualità, sottopixel, [Microsoft ClearType](/typography/cleartype/) che può utilizzare la tecnologia di rendering [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md)o specifica dell'applicazione.
- Testo con accelerazione hardware, se usato con [Direct2D](rendering-by-using-direct2d.md).
- Supporto per il testo in più formati.
- Supporto per le funzionalità tipografiche avanzate dei tipi di carattere OpenType.
- Supporto per il layout e il rendering del testo in tutte le lingue supportate.
- Layout e rendering compatibili con [GDI](interoperating-with-gdi.md).

L'API supporta la misurazione, il disegno e l'hit testing del testo in più formati. DirectWrite gestisce il testo in tutte le lingue supportate per le applicazioni globali e localizzate, basandosi sull'infrastruttura di linguaggio chiave disponibile in Windows 7. DirectWrite fornisce anche un'API di rendering dei glifi di basso livello per gli sviluppatori che vogliono eseguire l'elaborazione da Unicode a glifo e del layout.

> [!NOTE]
> Il [progetto Reunion](/windows/apps/project-reunion/) introduce una nuova versione di DirectWrite &mdash; denominata DWriteCore &mdash; che viene eseguita nelle versioni di Windows fino a Windows 8 e apre lo sportello per l'uso multipiattaforma. Per altri dettagli, vedere [Panoramica di DWriteCore](dwritecore-overview.md).

## <a name="run-time-requirements"></a>Requisiti di runtime

- Windows 7 o Windows Vista con Service Pack 2 (SP2) e aggiornamento della piattaforma per Windows Vista
- Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) e aggiornamento della piattaforma per Windows Server 2008

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [Novità di DirectWrite](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | Di seguito sono riportate alcune delle nuove aggiunte a DirectWrite. <br/> |
| [Guida per programmatori](programming-guide.md)<br/> | Negli argomenti seguenti viene fornita una panoramica dell'API DirectWrite.<br/> |
| [Riferimento API](reference.md)<br/> | Descrive l'API DirectWrite.<br/> |
| [Codice di esempio](samples.md)<br/> | Questa sezione contiene informazioni sui programmi di esempio per DirectWrite.<br/> |
