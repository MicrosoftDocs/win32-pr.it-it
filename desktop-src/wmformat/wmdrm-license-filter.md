---
title: WMDRM_LICENSE_FILTER struttura (Wmdrmsdk.h)
description: La struttura FILTRO LICENZE WMDRM \_ definisce i parametri di filtro da usare durante la creazione di \_ un'enumerazione delle licenze.
ms.assetid: 43bbbfdc-1ec4-44a6-8245-96853bbeea86
keywords:
- WMDRM_LICENSE_FILTER struttura windows Media Format
- struttura windows Media Format
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
ms.openlocfilehash: 94dc65758c7c5a25d31dd9fdb2d0fcd5cfa65debfff3defab4b88280a5ff3b3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698138"
---
# <a name="wmdrm_license_filter-structure"></a>Struttura DEL FILTRO LICENZE WMDRM \_ \_

La **struttura FILTRO LICENZE WMDRM \_ \_** definisce i parametri di filtro da usare durante la creazione di un'enumerazione delle licenze.

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

Specifica un ID chiave per cui filtrare le licenze. Nell'enumerazione verranno incluse solo le licenze con l'ID chiave specificato.

</dd> <dt>

**bstrRights**
</dt> <dd>

Specifica un set di diritti per cui filtrare le licenze. Nell'enumerazione verranno incluse solo le licenze che forniscono tutti i diritti specificati.

</dd> <dt>

**bstrAllowedSourceIDs**
</dt> <dd>

Specifica le origini del contenuto protetto da includere nella ricerca delle licenze.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene usata dal [**metodo IWMDRMLicenseManagement::CreateLicenseEnumeration.**](iwmdrmlicensemanagement-createlicenseenumeration.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





