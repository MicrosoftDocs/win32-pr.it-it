---
description: La sezione SourceDisksNames di un file INF identifica i dischi che contengono i file di origine installati.
ms.assetid: af4bc466-f0a3-4f83-adb7-6bfc276f7764
title: Esempio di sezioni SourceDisksNames e SourceDisksFiles di INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00eb8241b8e290f5460cc41b233d3b199df35e709d6e32f2c5a39925a79f851d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739411"
---
# <a name="inf-sourcedisksnames-and-sourcedisksfiles-sections-example"></a>Esempio di sezioni SourceDisksNames e SourceDisksFiles di INF

La **sezione SourceDisksNames** di un file INF identifica i dischi che contengono i file di origine installati. La **sezione SourceDisksFiles** identifica i file di origine e i dischi di origine che li contengono. Si noti che le piattaforme MIPS, Alpha e PPC non sono supportate da Windows 2000 o Windows XP.

A partire da Windows XP, una **sezione SourceDisksNames** può specificare un tag e un file cab. Ad esempio, la sezione **SourceDisksNames** seguente può essere usata con supporti rimovibili o fissi. Se si usano supporti rimovibili, la sezione di esempio verifica la presenza del supporto controllando prima la presenza del tag. Se si usano supporti fissi, la sezione di esempio verifica la presenza dei supporti verificando prima la presenza dell'archivio. Dopo aver verificato la presenza di un file cab, il sistema tenta di copiare i file dall'archivio e richiede tutti i file che non è stato possibile copiare.

``` syntax
[SourceDisksNames]
1="Dajava" , "Dajava.cab",,, 0x10,"Dajava.tag"
```

Per altre informazioni su **SourceDisksNames** o **SourceDisksFiles,** vedere le sezioni "Linee guida generali per file INF" e "Sezioni e direttive dei file INF" di Microsoft Windows 2000 Driver Development Kit.

 

 



