---
title: DirectWrite (DWrite)
description: Le applicazioni attuali devono supportare il rendering del testo di alta qualità, i tipi di carattere del contorno indipendenti dalla risoluzione e il supporto completo per layout e testo Unicode. DirectWrite, un'API [DirectX,](../directx.md) fornisce queste funzionalità e altro ancora.
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6bdc75845c2387a4fa4335fa462d0b97ec5669
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587949"
---
# <a name="directwrite-dwrite"></a>DirectWrite (DWrite)

## <a name="purpose"></a>Scopo

Le applicazioni attuali devono supportare il rendering del testo di alta qualità, i tipi di carattere del contorno indipendenti dalla risoluzione e il supporto completo per layout e testo Unicode. DirectWrite, un'API [DirectX,](../directx.md) fornisce queste funzionalità e altro ancora.

- Sistema di layout di testo indipendente dal dispositivo che migliora la leggibilità del testo nei documenti e nell'interfaccia utente.
- Rendering di testo [ClearType Microsoft di](/typography/cleartype/) alta qualità e secondario che può usare [GDI,](interoperating-with-gdi.md) [Direct2D](rendering-by-using-direct2d.md)o una tecnologia di rendering specifica dell'applicazione.
- Testo con accelerazione hardware, se usato con [Direct2D.](rendering-by-using-direct2d.md)
- Supporto per testo in più formati.
- Supporto per le funzionalità tipografiche avanzate dei tipi di carattere OpenType.
- Supporto per il layout e il rendering del testo in tutte le lingue supportate.
- Layout e rendering compatibili con [GDI.](interoperating-with-gdi.md)

L'API supporta la misurazione, il disegno e l'hit testing di testo in più formati. DirectWrite gestisce il testo in tutte le lingue supportate per le applicazioni globali e localizzate, sulla base dell'infrastruttura di lingua chiave disponibile in Windows 7. DirectWrite fornisce anche un'API di rendering dei glifi di basso livello per gli sviluppatori che vogliono eseguire l'elaborazione da Unicode a glifo e del layout.

> [!NOTE]
> [Windows App SDK](/windows/apps/windows-app-sdk/) introduce una nuova versione di DirectWrite denominata DWriteCore che viene eseguita nelle versioni di Windows fino a Windows 8 e apre la porta per l'uso &mdash; &mdash; multipiattaforma. Per altri dettagli, vedere [Panoramica di DWriteCore.](dwritecore-overview.md)

## <a name="run-time-requirements"></a>Requisiti di runtime

- Windows 7 o Windows Vista con Service Pack 2 (SP2) e Aggiornamento piattaforma per Windows Vista
- Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) e Aggiornamento della piattaforma per Windows Server 2008

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [Novità di DirectWrite](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | Ecco alcune delle nuove aggiunte a DirectWrite. <br/> |
| [Guida per programmatori](programming-guide.md)<br/> | Gli argomenti seguenti offrono una panoramica dell'API DirectWrite.<br/> |
| [Riferimento API](reference.md)<br/> | Descrive l'API DirectWrite.<br/> |
| [Codice di esempio](samples.md)<br/> | Questa sezione contiene informazioni sui programmi di esempio per DirectWrite.<br/> |
