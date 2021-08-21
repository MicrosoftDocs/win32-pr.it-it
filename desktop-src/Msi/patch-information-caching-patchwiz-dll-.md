---
description: La generazione di una nuova patch può richiedere tempo significativo.
ms.assetid: 8be9a83a-8c36-43f5-8dda-05fc2f3ce0d2
title: Patch Information Caching (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71513ea1a9418506bbf9025f66a1689c12e9a53f8e6f2e713ddeb3b3d55de580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942622"
---
# <a name="patch-information-caching-patchwizdll"></a>Patch Information Caching (Patchwiz.dll)

La generazione di una nuova patch può richiedere tempo significativo. Dopo aver generato una patch usando [Patchwiz.dll](patchwiz-dll.md), potrebbe essere necessario modificare nuovamente l'immagine di aggiornamento e generare un'altra patch. La memorizzazione nella cache delle informazioni sulle patch può ridurre il tempo necessario per generare patch successive riutilizzando le patch esistenti. Ad esempio, il tempo necessario per creare i Service Pack può essere ridotto usando le patch binarie generate dalle patch precedenti. Patchwiz.dll possibile usare PATCH CACHE DIR per trovare una patch binaria esistente e aggiungerla all'archivio del Service Pack senza dover creare \_ \_ nuovamente la patch binaria.

La memorizzazione nella cache delle informazioni sulle patch richiede [ l'Patchwiz.dll](patchwiz-dll.md). Per attivare la memorizzazione nella cache delle patch, impostare le proprietà PATCH CACHE ENABLED e PATCH CACHE DIR nella tabella delle proprietà (Patchwiz.dll) del file delle proprietà di creazione della \_ \_ patch \_ \_ (file con estensione pcp). [](properties-table-patchwiz-dll-.md) Patchwiz archivia tutte le informazioni di creazione della patch nella cartella identificata dalla proprietà PATCH CACHE DIR e \_ crea questa \_ cartella, se necessario. Al successivo tentativo di creare una patch, Patchwiz controlla questa cartella per verificare se i file da confrontare corrispondono ai file nella cache. Se i file corrispondono, Patchwiz usa le informazioni memorizzate nella cache anziché rigenerare la patch binaria per il file. Se i file non corrispondono o se le informazioni non sono presenti nella cache, Patchwiz genera la patch per il file.

Per usare la memorizzazione nella cache delle informazioni sulle patch, la cartella specificata da PATCH CACHE DIR deve essere mantenuta \_ dopo la creazione di un file con estensione \_ msp. Se la cartella viene eliminata, PatchWiz deve generare nuovamente patch binarie per i file msp successivi. Per altre informazioni sul mantenimento delle informazioni nelle aree selezionate di un file di destinazione, vedere Applicazione di patch alle [aree selezionate di un file](patching-selected-regions-of-a-file.md).

 

 



