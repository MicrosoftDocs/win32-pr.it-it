---
description: Le trasformazioni incorporate vengono archiviate all'interno del file con estensione msi del pacchetto. Ciò garantisce agli utenti che la trasformazione è sempre disponibile quando il pacchetto di installazione è disponibile. In alternativa, le trasformazioni possono essere fornite agli utenti come file con estensione MST autonomo.
ms.assetid: f7b265df-4b34-44ea-85ab-8dbca4797517
title: Trasformazioni incorporate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301e7f188da1a46411636ef90b7e6ae327a06c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050146"
---
# <a name="embedded-transforms"></a>Trasformazioni incorporate

Le trasformazioni incorporate vengono archiviate all'interno del file con estensione msi del pacchetto. Ciò garantisce agli utenti che la trasformazione è sempre disponibile quando il pacchetto di installazione è disponibile. In alternativa, le trasformazioni possono essere fornite agli utenti come file con estensione MST autonomo.

Per aggiungere una trasformazione incorporata all'elenco di trasformazioni, aggiungere i due punti (:) prefisso per il nome file. Poiché il programma di installazione può sempre ottenere la trasformazione dallo spazio di archiviazione nel file con estensione msi, le trasformazioni incorporate non vengono memorizzate nella cache nel computer dell'utente. Le trasformazioni incorporate possono essere utilizzate in combinazione con trasformazioni [protette](secured-transforms.md) o [trasformazioni non protette](unsecured-transforms.md). Per ulteriori informazioni, vedere [applicazione delle trasformazioni](applying-transforms.md).

 

 



