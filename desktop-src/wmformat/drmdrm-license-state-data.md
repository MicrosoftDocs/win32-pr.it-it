---
title: DRM_LICENSE_STATE_DATA struttura (Wmdrmsdk.h)
description: La struttura DRM \_ LICENSE STATE DATA contiene informazioni sulle restrizioni di licenza per un diritto \_ \_ DRM.
ms.assetid: 822d60ae-5d96-4577-8564-0e1adafa5dd5
keywords:
- DRM_LICENSE_STATE_DATA struttura windows Media Format
- Struttura windows Media Format
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63ba00384ec7c3340aa099f1b427cd8953969704bd0585f0da58cd4fd0ffd6ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708931"
---
# <a name="drm_license_state_data-structure-wmdrmsdkh"></a>DRM_LICENSE_STATE_DATA struttura (Wmdrmsdk.h)

La **struttura DRM \_ LICENSE STATE \_ \_ DATA** contiene informazioni sulle restrizioni di licenza per un diritto DRM.

## <a name="syntax"></a>Sintassi


```C++
typedef struct DRM_LICENSE_STATE_DATA {
  DWORD                      dwStreamId;
  DRM_LICENSE_STATE_CATEGORY dwCategory;
  DWORD                      dwNumCounts;
  DWORD                      dwCount[4];
  DWORD                      dwNumDates;
  FILETIME                   datetime[4];
  DWORD                      dwVague;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**dwStreamId**
</dt> <dd>

Numero di flusso a cui si applica la licenza. Deve essere 0, che indica che la licenza si applica a tutti i flussi nel file.

</dd> <dt>

**dwCategory**
</dt> <dd>

Categoria di stringa da visualizzare. Vedere [**DRM \_ LICENSE STATE \_ CATEGORY \_ per**](drmdrm-license-state-category.md) i valori possibili e il relativo significato.

</dd> <dt>

**dwNumCounts**
</dt> <dd>

Numero di elementi forniti in **dwCount**. Questo valore è in genere 0 o 1.

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

Matrice di 0 o 1 o più **valori DWORD** che rappresentano il numero di volte in cui può essere eseguita l'azione specificata in **dwCategory.** Vedere la sezione Osservazioni.

</dd> <dt>

**dwNumDates**
</dt> <dd>

Numero di elementi forniti in **datetime.** In genere non vengono usate più di due date, ad esempio con una licenza valida da una data a un'altra.

</dd> <dt>

**datetime \[ 4\]**
</dt> <dd>

Matrice di una o più **strutture FILETIME** che rappresentano una o più date nella licenza. Il significato di una data specifica dipende dal valore di **dwCategory**.

</dd> <dt>

**dwVague**
</dt> <dd>

Zero o più dei flag seguenti combinati con un'operazione OR bit per **bit:**



| Flag                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DATI SULLO STATO DELLE LICENZE DRM \_ \_ \_ \_ VAGHE        | Se impostato, potrebbero essere presenti più licenze che si applicano al contenuto. L'unico modo per essere certi delle singole licenze che si applicano a un DETERMINATO ID chiave è enumerare le licenze. A tale scopo, chiamare [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passando l'ID chiave come parametro bstrKID. Usare quindi l'interfaccia IWMDRMLicense recuperata per esaminare le licenze. |
| DRM \_ LICENSE \_ STATE \_ DATA \_ OPL \_ PRESENT | Se impostata, la licenza include i livelli di protezione dell'output (OPL) che devono essere recuperati e verificati rispetto alla destinazione dell'output dell'applicazione.                                                                                                                                                                                                                                                                                  |
| DRM \_ LICENSE \_ STATE \_ DATA \_ SAP \_ PRESENT | Se impostato, il contenuto deve essere recapitato usando un percorso audio sicuro (SAP).                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene recuperata chiamando **IWMDRMLicenseQuery::QueryLicenseState**.

Se **dwCategory** è **WM \_ DRM LICENSE STATE COUNT \_ FROM \_ \_ \_ \_ UNTIL**, la matrice **datetime** conterrà in genere due date: una data "da" e una data "fino a". È anche possibile specificare due coppie di date per creare licenze più complesse.

Gli elementi della matrice **dwCount** corrispondono alle date o agli intervalli di date specificati nella **matrice datetime.** Se **dwCategory è** **WM \_ DRM LICENSE STATE COUNT \_ \_ FROM \_ \_ \_ UNTIL** e **datetime** contiene una coppia di date, **dwCount** conterrà un elemento. Se **datetime** contiene due coppie di date (quattro elementi), **dwCount** deve contenere due elementi, uno per ogni coppia di date.

In alcuni casi, è possibile che agli utenti sia stata rilasciata più di una licenza per un file. Ad esempio, potrebbero aver acquisito una licenza che ha consentito cinque giochi fino alla fine del mese e successivamente acquisito una seconda licenza per diritti illimitati. In tal caso, il flag DRM LICENSE STATE DATA VAGUE è impostato \_ \_ in \_ \_ **dwVague** ( ) e il componente `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` DRM userà un algoritmo per determinare il set più probabile di diritti applicati. Alla scadenza di una licenza, il componente DRM esaminerà le licenze rimanenti e così via fino alla scadenza di tutte le licenze.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





