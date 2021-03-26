---
title: Informazioni sul file Memory-Mapped
description: Un file mappato alla memoria (o mapping di file) è il risultato dell'associazione del contenuto di un file a una parte dello spazio degli indirizzi virtuali di un processo. Può essere usato per condividere un file o una memoria tra due o più processi.
ms.assetid: b6ec2bc4-c504-4d0b-87f0-39bb1949accd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc6d33e7f3fe6bef36ea6e5a7f355b780d89b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118271"
---
# <a name="memory-mapped-file-information"></a>Informazioni sul file Memory-Mapped

Un *file mappato alla memoria* (o *mapping di file*) è il risultato dell'associazione del contenuto di un file a una parte dello spazio degli indirizzi virtuali di un processo. Può essere usato per condividere un file o una memoria tra due o più processi.

La funzione [**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea) riceve un handle di processo e un puntatore a un indirizzo come input. Se l'indirizzo si trova all'interno di un file mappato alla memoria nello spazio degli indirizzi virtuali del processo, la funzione restituisce il nome del file mappato alla memoria. I nomi di file restituiti da **GetMappedFileName** usano il modulo del dispositivo anziché le lettere di unità. Ad esempio, il nome del file c: \\ WinNT \\ system32 \\ . nls avrà un aspetto simile al seguente nel modulo del dispositivo:

\\Device \\ DiscoRigido0 \\ Partition1 \\ WinNT \\ system32 \\ . nls

Per ulteriori informazioni sui file mappati alla memoria, vedere [mapping di file](/windows/desktop/Memory/file-mapping). Per un esempio in cui i nomi di file vengono convertiti in formato dispositivo in lettere di unità, vedere [ottenere un nome di file da un handle di file](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle).

 

 