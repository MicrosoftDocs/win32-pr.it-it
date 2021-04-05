---
title: CENUMOBJ. CPP
description: Nel componente provider di esempio, l'enumerazione di un oggetto contenitore usa le routine, da cenumobj. cpp, elencate nella tabella seguente.
ms.assetid: 7166230d-0bf8-4f7d-9781-72f125a3dd21
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b7859571c7136cf1f8a2895b69fe7cdcdf07604
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730194"
---
# <a name="cenumobjcpp"></a>CENUMOBJ. CPP

Nel componente provider di esempio, l'enumerazione di un oggetto contenitore usa le routine, da cenumobj. cpp, elencate nella tabella seguente.



| Metodo                                                 | Descrizione                                                                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSGenObjectEnum:: create**                     | Creare un oggetto per abilitare l'enumerazione degli oggetti Active Directory generici.                                                                                           |
| **CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**     | Inizializzazione.                                                                                                                                                       |
| **CSampleDSGenObjectEnum::EnumGenericObjects**         | Gestire il recupero di oggetti.                                                                                                                                          |
| **CSampleDSGenObjectEnum::FetchObjects**               | Recuperare il set di puntatori [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che corrispondono al filtro.                                                             |
| **CSampleDSGenObjectEnum::FetchNextObject**            | Recuperare un oggetto e confrontarlo con il filtro. Se corrisponde a, eseguire il wrapping in un oggetto generico e restituire un puntatore [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . |
| **CSampleDSGenObjectEnum::EnumGenericObjects**         | Gestire il recupero degli oggetti.                                                                                                                                        |
| **CSampleDSGenObjectEnum:: Next**                       | Recupera il numero specificato di elementi dall'oggetto di enumerazione indicato.                                                                                      |
| **CSampleDSGenObjectEnum::IsValidDSFilter**            | Verificare che la classe di oggetti corrisponda a una nell'elenco di filtri.                                                                                                              |
| **CSampleDSGenObjectEnum::BuildDSFilterArray**         | Gestire la matrice di filtri.                                                                                                                                              |
| **CSampleDSGenObjectEnum::CreateAndAppendFilterEntry** | Aggiungere una nuova classe di oggetti al filtro e impostare il filtro come contiguo.                                                                                                |
| **FreeFilterList**                                     | Liberare il filtro.                                                                                                                                                      |



 

 

 