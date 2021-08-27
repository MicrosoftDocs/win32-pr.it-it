---
title: Definizione delle categorie di componenti
description: Definizione delle categorie di componenti
ms.assetid: 2d67a998-5200-4285-bd99-48cf59683569
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840c785f4b263f0288793f62542cc6d93637b719ff37c9cf29454f43dfaa1914
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071011"
---
# <a name="defining-component-categories"></a>Definizione delle categorie di componenti

L'autore di una definizione di categoria di componenti crea un GUID univoco (CATID) pubblicato insieme alla definizione. Altre parti conoscono la definizione di questo tipo e possono usare le classi supportate di conseguenza. Analogamente alla firma del metodo di un'interfaccia, la semantica di una categoria non deve essere modificata dopo l'installazione. È meglio mantenere la compatibilità con le versioni precedenti della categoria introducendo un nuovo identificatore di categoria con semantica modificata.

Poiché gli identificatori di interfaccia (IID) e gli identificatori di categoria del componente (CATID) esistono in spazi dei nomi diversi, sembra che sia possibile usare lo stesso GUID sia per un IID che per un CATID. Tuttavia, poiché gli IID vengono spesso usati per il CLSID del server proxy/stub dell'interfaccia, è possibile che si sia verificata una conflitto. Pertanto, non usare lo stesso GUID per un IID e un CATID.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Associazione di icone a una categoria](associating-icons-with-a-category.md)
</dt> <dt>

[Categorizzazione in base alle funzionalità dei componenti](categorizing-by-component-capabilities.md)
</dt> <dt>

[Categorizzazione in base alle funzionalità del contenitore](categorizing-by-container-capabilities.md)
</dt> <dt>

[Classi e associazioni predefinite](default-classes-and-associations.md)
</dt> <dt>

[Gestione categorie componenti](the-component-categories-manager.md)
</dt> </dl>

 

 




