---
description: La generazione di una nuova patch potrebbe richiedere un tempo significativo.
ms.assetid: 8be9a83a-8c36-43f5-8dda-05fc2f3ce0d2
title: Caching delle informazioni sulla patch (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7000efceea62e9eef122a34f7700622e1e6e2e60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309465"
---
# <a name="patch-information-caching-patchwizdll"></a>Caching delle informazioni sulla patch (Patchwiz.dll)

La generazione di una nuova patch potrebbe richiedere un tempo significativo. Dopo aver generato una patch usando [Patchwiz.dll](patchwiz-dll.md), potrebbe essere necessario modificare nuovamente l'immagine di aggiornamento e generare un'altra patch. La memorizzazione nella cache delle informazioni sulla patch può ridurre il tempo necessario per generare patch successive riutilizzando le patch esistenti. Ad esempio, è possibile ridurre il tempo necessario per creare Service Pack usando le patch binarie generate dalle patch precedenti. Patchwiz.dll possibile utilizzare \_ \_ la directory della cache delle patch per trovare una patch binaria esistente e aggiungerla al cabinet del Service Pack senza dover ricreare la patch binaria.

La memorizzazione nella cache delle informazioni sulla patch richiede l'uso di [Patchwiz.dll](patchwiz-dll.md). Per attivare la memorizzazione nella cache delle patch, impostare le \_ Proprietà patch cache \_ Enabled e patch \_ cache \_ dir nella [tabella Properties (Patchwiz.dll)](properties-table-patchwiz-dll-.md) del file delle proprietà della patch Creation (file con estensione PCP). Patchwiz archivia tutte le informazioni sulla creazione della patch nella cartella identificata \_ dalla \_ Proprietà dir della patch cache e crea questa cartella, se necessario. Al successivo tentativo di creazione di una patch, Patchwiz controlla questa cartella per verificare se i file da confrontare corrispondono ai file nella cache. Se i file corrispondono, Patchwiz usa le informazioni memorizzate nella cache anziché rigenerare la patch binaria per il file. Se i file non corrispondono o se le informazioni non sono presenti nella cache, Patchwiz genera la patch per il file.

Per utilizzare la memorizzazione nella cache delle informazioni sulla patch, è necessario conservare la cartella specificata da PATCH \_ cache \_ dir dopo la creazione di un file con estensione msp. Se la cartella viene eliminata, PatchWiz deve rigenerare le patch binarie per i successivi file con estensione msp. Per ulteriori informazioni sulla conservazione delle informazioni nelle aree selezionate di un file di destinazione, vedere applicazione [di patch alle aree selezionate di un file](patching-selected-regions-of-a-file.md).

 

 



