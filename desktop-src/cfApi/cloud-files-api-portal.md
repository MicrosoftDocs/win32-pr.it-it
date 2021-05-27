---
description: L'API Filtro cloud offre funzionalità al limite tra la modalità utente e la file system.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Motori di sincronizzazione cloud
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: d40b195a442859441138ae4e61cb0eb946411623
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549596"
---
# <a name="cloud-sync-engines"></a>Motori di sincronizzazione cloud

Vedere anche [l'esempio cloud mirror](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample).

A partire da Windows 10 versione 1709, Windows fornisce *l'API dei file cloud*. Questa API è costituita da diverse API Win32 e WinRT native che formalizzano il supporto per i motori di sincronizzazione cloud e gestiscono attività quali la creazione e la gestione di file segnaposto e directory. Gli utenti di questa API sono in genere provider di sincronizzazione e, in una certa misura, applicazioni Windows.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento                                                                | Descrizione                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Creare un motore di sincronizzazione cloud che supporti i file segnaposto](build-a-cloud-file-sync-engine.md)<br/> | Informazioni su come usare l'API file cloud per creare un motore di sincronizzazione file cloud che include file segnaposto e Esplora file integrazione. <br/> |
| [Informazioni di riferimento sul filtro cloud](cloud-filter-reference.md)<br/> | L'API di filtro cloud è un'API Win32 nativa che fa parte dell'API di file cloud più ampia. L'API filtro cloud fornisce funzionalità al limite tra la modalità utente e l'file system. Questa API gestisce la creazione e la gestione di file segnaposto e directory. <br/> |