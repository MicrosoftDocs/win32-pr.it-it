---
description: Per ottenere un elenco completo dei volumi in un computer o per modificare ogni volume a sua volta, è possibile enumerare i volumi.
ms.assetid: 5adcd59a-48b7-4373-a10b-c352962f715a
title: Enumerazione dei volumi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc294d72fa3fad24536b175ee7e5e023066586c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313884"
---
# <a name="enumerating-volumes"></a>Enumerazione dei volumi

Per ottenere un elenco completo dei volumi in un computer o per modificare ogni volume a sua volta, è possibile enumerare i volumi. All'interno di un volume, è possibile [analizzare le cartelle montate](enumerating-volume-mount-points.md) o altri oggetti nel volume.

Tre funzioni consentono a un'applicazione di enumerare i volumi in un computer:

-   [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)

Queste tre funzioni funzionano in modo molto simile alle funzioni [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)e [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .

Inizia una ricerca di volumi con [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew). Se la ricerca ha esito positivo, elaborare i risultati in base alla progettazione dell'applicazione. Usare quindi [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) in un ciclo per individuare ed elaborare ogni volume successivo. Quando viene esaurita la quantità di volumi, chiudere la ricerca con [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).

Non è consigliabile presupporre alcuna correlazione tra l'ordine dei volumi restituiti da queste funzioni e l'ordine dei volumi restituiti da altre funzioni o strumenti. In particolare, non presupporre alcuna correlazione tra l'ordine del volume e le lettere di unità assegnate dal BIOS (se presente) o dall'amministratore del disco.

Vedere [esempi di cartelle montate](volume-mount-point-examples.md) per un esempio su come enumerare i volumi in un computer.

 

 



