---
description: Indica la posizione in cui eseguire la ricerca di un Active Directory archivio certificati.
ms.assetid: 56b9695e-7ab9-405b-9cae-d78c43071186
title: Enumerazione CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: cd630bdc0c09a6bb57a9163ec972451011f3e826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326042"
---
# <a name="capicom_active_directory_search_location-enumeration"></a>\_Enumerazione del percorso di ricerca di Active \_ directory di \_ CAPICOM \_

Il tipo di enumerazione del **\_ percorso di ricerca di Active \_ directory \_ \_ di CAPICOM** indica la posizione in cui eseguire la ricerca di un [*archivio certificati*](../secgloss/c-gly.md)Active Directory.

## <a name="members"></a>Membri



| Membro                               | Descrizione                                  | Valore |
|--------------------------------------|----------------------------------------------|-------|
| **\_ricerca CAPICOM \_**             | Cerca tutti i percorsi disponibili.<br/> | 0     |
| **\_catalogo globale di ricerca \_ CAPICOM \_** | Esegue la ricerca solo nel catalogo globale.<br/> | 1     |
| **\_dominio predefinito di ricerca di CAPICOM \_ \_** | Cerca solo il dominio predefinito.<br/> | 2     |



## <a name="remarks"></a>Commenti

Questo tipo di enumerazione viene usato dalla proprietà seguente:

-   [**Settings. ActiveDirectorySearchLocation**](settings-activedirectorysearchlocation.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
