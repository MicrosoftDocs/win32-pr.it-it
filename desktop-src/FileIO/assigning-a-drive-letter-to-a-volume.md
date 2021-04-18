---
description: 'È possibile assegnare una lettera di unità (ad esempio, X: \) a un volume locale usando la funzione SetVolumeMountPoint, a condizione che non sia già stato assegnato un volume a tale lettera di unità.'
ms.assetid: 8c78b2e8-199a-4934-a9c4-6f3913f44efe
title: Assegnazione di una lettera di unità a un volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f31b9446cc41ad26f14a34874c59e153e1db8ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310039"
---
# <a name="assigning-a-drive-letter-to-a-volume"></a>Assegnazione di una lettera di unità a un volume

È possibile assegnare una lettera di unità (ad esempio, X: \) a un volume locale usando la funzione [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , a condizione che non sia già stato assegnato un volume a tale lettera di unità. Se il volume locale dispone già di una lettera di unità. quindi [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) avrà esito negativo. Per gestire questa operazione, eliminare innanzitutto la lettera di unità utilizzando la funzione [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) . Per un esempio di codice, vedere [modifica delle assegnazioni di lettere di unità](editing-drive-letter-assignments.md).

Il sistema supporta al massimo una lettera di unità per ogni volume. Pertanto, non è possibile avere C: \\ e F: \\ rappresentano lo stesso volume.

> [!Caution]
>
> Per eliminare una lettera di unità esistente e assegnarne una nuova, è possibile che si verifichino interruzioni dei percorsi esistenti, ad esempio quelli nei collegamenti desktop. Potrebbe inoltre interrompere il percorso del programma che rende la lettera di unità modificata. Con la gestione della memoria virtuale di Windows, questa operazione potrebbe interrompere l'applicazione, lasciando il sistema in uno stato instabile ed eventualmente inutilizzabile. È responsabilità del progettista del programma evitare tali catastrofi potenziali.

 

 

 



