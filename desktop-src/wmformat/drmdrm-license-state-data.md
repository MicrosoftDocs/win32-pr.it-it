---
title: Struttura DRM_LICENSE_STATE_DATA (wmdrmsdk. h)
description: La \_ \_ struttura dei dati di stato delle licenze DRM \_ contiene informazioni sulle restrizioni di licenza per un diritto DRM.
ms.assetid: 822d60ae-5d96-4577-8564-0e1adafa5dd5
keywords:
- Formato di Windows Media per la struttura DRM_LICENSE_STATE_DATA
- struttura Windows Media Format
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
ms.openlocfilehash: b02f38b8f09b7b444949e9477635e6b8770fc168
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330587"
---
# <a name="drm_license_state_data-structure-wmdrmsdkh"></a>Struttura DRM_LICENSE_STATE_DATA (wmdrmsdk. h)

La **struttura \_ \_ \_ dei dati di stato delle licenze DRM** contiene informazioni sulle restrizioni di licenza per un diritto DRM.

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

Numero di flusso a cui si applica la licenza. Deve essere 0, che indica che la licenza viene applicata a tutti i flussi del file.

</dd> <dt>

**dwCategory**
</dt> <dd>

Categoria di stringa da visualizzare. Vedere [**la \_ \_ \_ categoria dello stato della licenza DRM**](drmdrm-license-state-category.md) per i valori possibili e il relativo significato.

</dd> <dt>

**dwNumCounts**
</dt> <dd>

Numero di elementi forniti in **dwCount**. Questo valore è in genere 0 o 1.

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

Matrice di 0 o 1 o più valori **DWORD** che rappresentano il numero di volte in cui è possibile eseguire l'azione specificata in **dwCategory** . Vedere la sezione Osservazioni.

</dd> <dt>

**dwNumDates**
</dt> <dd>

Numero di elementi forniti in **DateTime**. In genere, non vengono usate più di due date, ad esempio, con una licenza valida da una data fino a un'altra data.

</dd> <dt>

**DateTime \[ 4\]**
</dt> <dd>

Matrice di una o più strutture **FILETIME** che rappresentano una o più date nella licenza. Il significato di una determinata data dipende dal valore di **dwCategory**.

</dd> <dt>

**dwVague**
</dt> <dd>

Zero o più dei flag seguenti combinati con un **or** bit per bit:



| Flag                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_dati di stato della licenza DRM \_ \_ \_ vaghi        | Se impostato, potrebbero essere presenti più licenze valide per il contenuto. L'unico modo per essere certi sulle singole licenze che si applicano a un ID chiave specifico è enumerare le licenze. A tale scopo, chiamare [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passando l'ID chiave come parametro bstrKID. Usare quindi l'interfaccia IWMDRMLicense recuperata per esaminare le licenze. |
| \_OPL dati di stato della licenza DRM \_ \_ \_ \_ presenti | Se impostata, la licenza include i livelli di protezione dell'output (OPLs) che devono essere recuperati e controllati rispetto alla destinazione dell'output dell'applicazione.                                                                                                                                                                                                                                                                                  |
| \_ \_ \_ \_ SAP presente dati di stato delle licenze DRM \_ | Se impostato, il contenuto deve essere recapitato usando il percorso audio sicuro (SAP).                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene recuperata chiamando **IWMDRMLicenseQuery:: QueryLicenseState**.

Se **dwCategory** è **il \_ \_ \_ conteggio dello stato di licenza WM DRM \_ \_ da \_ fino a**, la matrice **DateTime** conterrà in genere due date: una data "from" e una data "until". È anche possibile specificare due coppie di date per creare licenze più complesse.

Gli elementi della matrice **dwCount** corrispondono agli intervalli di date o date specificati nella matrice **DateTime** . Se **dwCategory** è **il \_ \_ \_ conteggio dello stato di licenza WM DRM \_ \_ da \_ until** e **DateTime** contiene una coppia di date, **dwCount** conterrà un elemento. Se **DateTime** contiene due coppie di date (quattro elementi), **dwCount** deve contenere due elementi, uno per ogni coppia di date.

In alcuni casi, è possibile che agli utenti sia stata rilasciata più di una licenza per un file. Potrebbero ad esempio avere acquisito una licenza che consentiva cinque Play fino alla fine del mese e successivamente ha acquisito una seconda licenza per diritti illimitati. In tal caso, il \_ \_ flag di dati dello stato delle licenze DRM \_ \_ è impostato in **dwVague** ( `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` ) e il componente DRM utilizzerà un algoritmo per determinare il set di diritti più probabile applicato. Quando una licenza scade, il componente DRM esaminerà le licenze rimanenti e così via fino a quando tutte le licenze non saranno scadute.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





