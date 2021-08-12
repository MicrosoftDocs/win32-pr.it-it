---
description: L'API filtro cloud fornisce funzionalità al limite tra la modalità utente e la file system.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Motori di sincronizzazione cloud
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: 39dd28779c07dfd6e44fde0e53f583e72971d5883205f42581e3b5ac4102c0eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551375"
---
# <a name="cloud-sync-engines"></a>Motori di sincronizzazione cloud

Vedere anche [l'esempio di mirroring del cloud.](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample)

A partire Windows 10 versione 1709, Windows *l'API dei file cloud*. Questa API è costituita da diverse API Win32 e WinRT native che formalizzano il supporto per i motori di sincronizzazione cloud e gestiscono attività come la creazione e la gestione di file e directory segnaposto. Gli utenti di questa API sono in genere provider di sincronizzazione e, in una certa misura, Windows applicazioni.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento                                                                | Descrizione                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Creare un motore di sincronizzazione cloud che supporta i file segnaposto](build-a-cloud-file-sync-engine.md)<br/> | Informazioni su come usare l'API dei file cloud per creare un motore di sincronizzazione file cloud che include file segnaposto e Esplora file integrazione. <br/> |
| [Informazioni di riferimento sul filtro cloud](cloud-filter-reference.md)<br/> | L'API di filtro cloud è un'API Win32 nativa che fa parte dell'API di file cloud più ampia. L'API di filtro cloud fornisce funzionalità al limite tra la modalità utente e la file system. Questa API gestisce la creazione e la gestione di file e directory segnaposto. <br/> |