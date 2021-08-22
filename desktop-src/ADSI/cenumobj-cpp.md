---
title: CENUMOBJ. CPP
description: Nel componente provider di esempio l'enumerazione di un oggetto contenitore usa le routine di cenumobj.cpp elencate nella tabella seguente.
ms.assetid: 7166230d-0bf8-4f7d-9781-72f125a3dd21
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad1e91a58080dc11f7d8da11f3e3fd59dc2ce75431ee2998d8d4e11011bbb32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023679"
---
# <a name="cenumobjcpp"></a>CENUMOBJ. CPP

Nel componente provider di esempio l'enumerazione di un oggetto contenitore usa le routine di cenumobj.cpp elencate nella tabella seguente.



| Metodo                                                 | Descrizione                                                                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSGenObjectEnum::Create**                     | Creare un oggetto per abilitare l'enumerazione di oggetti Active Directory generici.                                                                                           |
| **CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**     | Inizializzazione.                                                                                                                                                       |
| **CSampleDSGenObjectEnum::EnumGenericObjects**         | Gestire il recupero degli oggetti.                                                                                                                                          |
| **CSampleDSGenObjectEnum::FetchObjects**               | Recuperare il set di [**puntatori IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che corrispondono al filtro.                                                             |
| **CSampleDSGenObjectEnum::FetchNextObject**            | Recuperare un oggetto e trovare una corrispondenza con il filtro. Se corrisponde, eseguire il wrapping in un oggetto generico e restituire un [**puntatore IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) |
| **CSampleDSGenObjectEnum::EnumGenericObjects**         | Gestire il recupero degli oggetti.                                                                                                                                        |
| **CSampleDSGenObjectEnum::Next**                       | Recupera il numero specificato di elementi dall'oggetto enumerazione indicato.                                                                                      |
| **CSampleDSGenObjectEnum::IsValidDSFilter**            | Verificare che la classe di oggetti corrisponda a una classe nell'elenco di filtri.                                                                                                              |
| **CSampleDSGenObjectEnum::BuildDSFilterArray**         | Gestire la matrice di filtri.                                                                                                                                              |
| **CSampleDSGenObjectEnum::CreateAndAppendFilterEntry** | Aggiungere una nuova classe di oggetti al filtro e impostare il filtro come contiguo.                                                                                                |
| **FreeFilterList**                                     | Liberare il filtro.                                                                                                                                                      |



 

 

 