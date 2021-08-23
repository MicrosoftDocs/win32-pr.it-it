---
description: 'È possibile assegnare una lettera di unità ,ad esempio X: a un volume locale usando la funzione SetVolumeMountPoint, a condizione che non sia già stato assegnato alcun volume a tale lettera \) di unità.'
ms.assetid: 8c78b2e8-199a-4934-a9c4-6f3913f44efe
title: Assegnazione di una lettera di unità a un volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6cc2e894580a394e73896291f05a2f54c615949bfeb63ea3e574deef1353d91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766224"
---
# <a name="assigning-a-drive-letter-to-a-volume"></a>Assegnazione di una lettera di unità a un volume

È possibile assegnare una lettera di unità ,ad esempio X: a un volume locale usando la \) [**funzione SetVolumeMountPoint,**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) a condizione che non sia già stato assegnato alcun volume a tale lettera di unità. Se il volume locale ha già una lettera di unità. Quindi [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) avrà esito negativo. Per gestire questo problema, eliminare prima di tutto la lettera di unità usando [**la funzione DeleteVolumeMountPoint.**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) Per un esempio di codice, vedere [Modifica delle assegnazioni delle lettere di unità.](editing-drive-letter-assignments.md)

Il sistema supporta al massimo una lettera di unità per volume. Pertanto, non è possibile fare in \\ modo che C: e F: \\ rappresentino lo stesso volume.

> [!Caution]
>
> L'eliminazione di una lettera di unità esistente e l'assegnazione di una nuova lettera potrebbero interrompere i percorsi esistenti, ad esempio quelli nei collegamenti del desktop. Può anche interrompere il percorso del programma che apporta modifiche alla lettera di unità. Con Windows della memoria virtuale, questa operazione potrebbe causare l'interruzione dell'applicazione, lasciando il sistema in uno stato instabile e possibilmente inutilizzabile. È responsabilità del progettista del programma evitare tali potenziali catastrofi.

 

 

 



