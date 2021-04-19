---
description: L'API di filtro cloud fornisce funzionalità al limite tra la modalità utente e la file system.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Motori di sincronizzazione cloud
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: debe32a1849a393a067017f90f5405c4b3ba77d1
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323891"
---
# <a name="cloud-sync-engines"></a>Motori di sincronizzazione cloud

Vedere anche [esempio di mirroring cloud](/windows/win32/cfapi/build-a-cloud-file-sync-engine#cloud-mirror-sample).

A partire da Windows 10, versione 1709, Windows fornisce l' *API per i file Cloud*. Questa API è costituita da diverse API Win32 e WinRT native che formalizzano il supporto per i motori di sincronizzazione cloud e gestisce attività quali la creazione e la gestione di file e directory segnaposto. Gli utenti di questa API sono in genere provider di sincronizzazione e in qualche misura le applicazioni Windows.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento                                                                | Descrizione                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Creare un motore di sincronizzazione cloud che supporti i file segnaposto](build-a-cloud-file-sync-engine.md)<br/> | Informazioni su come usare l'API file cloud per compilare un motore di sincronizzazione file cloud che include file segnaposto e integrazione con Esplora file. <br/> |
| [Riferimento al filtro cloud](cloud-filter-reference.md)<br/> | L'API di filtro cloud è un'API Win32 nativa che fa parte dell'API file cloud più ampia. L'API di filtro cloud fornisce funzionalità al limite tra la modalità utente e la file system. Questa API gestisce la creazione e la gestione di file e directory segnaposto. <br/> |

