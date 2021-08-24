---
description: Set di proprietà
ms.assetid: 4b8a917f-7a6c-4433-83f4-b83ef6d26115
title: Set di proprietà (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c26bef876e0bde559ac506963f86a485a302a9ce6faf6c2699c62dabac3f72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747951"
---
# <a name="property-sets-directshow"></a>Set di proprietà (DirectShow)

Microsoft DirectShow usa set di proprietà per supportare i servizi estesi offerti dall'hardware e i relativi driver e filtri associati. I fornitori di hardware e filtri possono definire nuove funzionalità come proprietà, disponerle in set di proprietà e pubblicare la specifica per questi set di proprietà. Lo sviluppatore dell'applicazione può usare i metodi [**dell'interfaccia IKsPropertySet**](ikspropertyset.md) per determinare se un driver o un filtro supporta un determinato set di proprietà e recuperare o impostare tali proprietà.

Tutti i metodi esposti da **IKsPropertySet** richiedono un **GUID** che identifica il set di proprietà (parametro *guidPropSet)* e un **valore DWORD** che identifica la proprietà all'interno del set di proprietà *(parametro dwPropID).* Il *parametro dwPropID* è in genere un membro di un tipo di dati enumerato.

Alle singole proprietà possono essere associati dati specificati nel *parametro pPropData* nei metodi [**IKsPropertySet::Set**](ikspropertyset-set.md) e [**IKsPropertySet::Get.**](ikspropertyset-get.md) In questi metodi i dati della proprietà vengono tipiati come puntatore a `void` . Il tipo di dati e il significato dei dati vengono specificati nella definizione del set di proprietà.

Le sezioni seguenti forniscono informazioni sui set di proprietà supportati in DirectShow:

-   [**Set di proprietà protezione copia DVD**](dvd-copy-protection-property-set.md)
-   [**Set di proprietà DVD Per dvd**](dvd-karaoke-property-set.md)
-   [**Set di proprietà Dvd Subpicture**](dvd-subpicture-property-set.md)
-   [Set di proprietà Trasporto dispositivo esterno](external-device-transport-property-set.md)
-   [Set di proprietà Frame Stepping](frame-stepping-property-set.md)
-   [Impostare la proprietà Pin](pin-property-set.md)
-   [**Impostare le proprietà di modifica della frequenza**](rate-change-property-set.md)

 

 



