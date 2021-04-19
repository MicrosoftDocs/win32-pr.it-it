---
title: Struttura WMDRM_LICENSE_FILTER (wmdrmsdk. h)
description: La \_ struttura del filtro delle licenze WMDRM definisce i \_ parametri di filtro da usare durante la creazione di un'enumerazione delle licenze.
ms.assetid: 43bbbfdc-1ec4-44a6-8245-96853bbeea86
keywords:
- Formato di Windows Media per la struttura WMDRM_LICENSE_FILTER
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRM_LICENSE_FILTER
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200bea0d74b7c9a84c5731072e2e65bca81b6cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326599"
---
# <a name="wmdrm_license_filter-structure"></a>Struttura del filtro delle \_ licenze WMDRM \_

La struttura del **\_ \_ filtro delle licenze WMDRM** definisce i parametri di filtro da usare durante la creazione di un'enumerazione delle licenze.

## <a name="syntax"></a>Sintassi


```C++
typedef struct WMDRM_LICENSE_FILTER {
  DWORD dwVersion;
  BSTR  bstrKID;
  BSTR  bstrRights;
  BSTR  bstrAllowedSourceIDs;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**dwVersion**
</dt> <dd>

Specifica un numero di versione minimo per le licenze restituite.

</dd> <dt>

**bstrKID**
</dt> <dd>

Specifica un ID chiave per il filtro delle licenze. Nell'enumerazione verranno incluse solo le licenze con l'ID chiave specificato.

</dd> <dt>

**bstrRights**
</dt> <dd>

Specifica un set di diritti per filtrare le licenze per. Nell'enumerazione verranno incluse solo le licenze che forniscono tutti i diritti specificati.

</dd> <dt>

**bstrAllowedSourceIDs**
</dt> <dd>

Specifica le origini del contenuto protetto da includere nella ricerca di licenze.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata dal metodo [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





