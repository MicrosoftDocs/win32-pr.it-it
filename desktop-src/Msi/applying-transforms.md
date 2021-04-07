---
description: La proprietà Transforms contiene l'elenco di trasformazioni per un pacchetto di installazione. Il programma di installazione applica tutte le trasformazioni nell'elenco delle trasformazioni a ogni installazione, annuncio, installazione su richiesta o installazione di manutenzione del pacchetto.
ms.assetid: dde2ef55-7794-4eb1-984a-ed13e990c97f
title: Applicazione di trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2367e02396ec33e517f8abfe579060c0a0986be2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881121"
---
# <a name="applying-transforms"></a>Applicazione di trasformazioni

La proprietà [**TRANSforms**](transforms.md) contiene l'elenco di trasformazioni per un pacchetto di installazione. Il programma di installazione applica tutte le trasformazioni nell'elenco delle trasformazioni a ogni installazione, annuncio, installazione su richiesta o installazione di manutenzione del pacchetto.

La proprietà [**TRANSforms**](transforms.md) viene impostata specificando l'elenco di trasformazioni nella riga di comando. Tuttavia, quando si utilizza l' [opzione della riga di comando](command-line-options.md)/JM o/Ju, è necessario specificare l'elenco di trasformazioni utilizzando l'opzione/t.

Si noti che l'elenco di trasformazioni non può essere modificato una volta installato e può essere rimosso solo disinstallando l'applicazione.

> [!Note]  
> Un pacchetto di Windows Installer può applicare non più di 255 trasformazioni durante l'installazione di un'applicazione o di un aggiornamento. Quando sono necessarie numerose trasformazioni, devono essere combinate e le trasformazioni obsolete precedenti devono essere eliminate.

 

Nella tabella seguente vengono forniti esempi di diverse stringhe di trasformazioni che è possibile aggiungere all'elenco Transformations.



| Trasforma stringa                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| transform1. MST;: transform2. MST;: transform3. MST                                                                                 | Transform2. MST e transform3. MST sono [trasformazioni incorporate](embedded-transforms.md). transform1. MST è una [trasformazione sicura a livello di origine](secure-at-source-transforms.md) solo se è impostata la proprietà [**TRANSFORMSSECURE**](transformssecure.md) o il [criterio TRANSFORMSSECURE](transformssecure-policy.md) ; in caso contrario, transform1 è una [trasformazione non protetta](unsecured-transforms.md). |
| \\\\\\percorso condivisione \\ server \\ transform1. MST;: transform2. MST                                                                        | Transform2. MST è una [trasformazione incorporata](embedded-transforms.md). transform1. MST è una [trasformazione protetta con percorso completo](secure-full-path-transforms.md) solo se la proprietà [**TRANSFORMSSECURE**](transformssecure.md) o il [criterio TRANSFORMSSECURE](transformssecure-policy.md) è impostato; in caso contrario, transform1 è una [trasformazione non protetta](unsecured-transforms.md).                   |
| @: transform2. MST; transform1. MST @transform1.mst ;: transform2. MST<br/>                                                     | Transform2. MST è una trasformazione incorporata. transform1. MST è una [trasformazione protetta all'origine](secure-at-source-transforms.md)autonoma.                                                                                                                                                                                                                                                |
| \|\\\\\\percorso condivisione \\ server \\ transform1. MST;: transform2. MST \| : transform2. MST; \\ \\ \\percorso condivisione \\ server \\ transform1. MST<br/> | Transform2. MST è una trasformazione incorporata. transform1. MST è una [trasformazione protetta con percorso completo](secure-full-path-transforms.md)autonomo.                                                                                                                                                                                                                                                 |



 

 

 




