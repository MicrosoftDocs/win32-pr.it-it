---
title: Struttura DRM_LICENSE_STATE_DATA (Drmexternals. h)
description: La \_ \_ \_ struttura dei dati di stato della licenza DRM contiene informazioni sulle licenze relative a un diritto DRM specificato.
ms.assetid: 5ca577b5-d28b-4e36-8af7-6fae4300d464
keywords:
- Formato di Windows Media per la struttura DRM_LICENSE_STATE_DATA
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bb63bce02a52aefcf1f3351fe34ab008996aa0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302062"
---
# <a name="drm_license_state_data-structure-drmexternalsh"></a>Struttura DRM_LICENSE_STATE_DATA (Drmexternals. h)

La **struttura \_ \_ \_ dei dati di stato della licenza DRM** contiene informazioni sulle [*licenze*](wmformat-glossary.md) relative a un diritto [*DRM*](wmformat-glossary.md) specificato.

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

Categoria di stringa da visualizzare. Vedere [**la \_ \_ \_ categoria dello stato della licenza DRM**](drm-license-state-category.md) per i valori possibili e il relativo significato.

</dd> <dt>

**dwNumCounts**
</dt> <dd>

Numero di elementi forniti in **dwCount**. Questo valore è in genere 0 o 1.

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

Matrice di 0 o 1 o più **DWORD** che rappresenta il numero di volte in cui è possibile eseguire l'azione specificata in **dwCategory** . Vedere la sezione Osservazioni.

</dd> <dt>

**dwNumDates**
</dt> <dd>

Numero di elementi forniti in **DateTime**. In genere, non vengono usate più di due date, ad esempio, con una licenza valida da una data fino a un'altra data.

</dd> <dt>

**DateTime \[ 4\]**
</dt> <dd>

Matrice di una o più strutture FILETIME che rappresentano una o più date nella licenza. Il significato di una determinata data dipende dal valore di **dwCategory**.

</dd> <dt>

**dwVague**
</dt> <dd>

Zero o più dei flag seguenti combinati con un **or** bit per bit:



| Flag                                    | Descrizione                                                                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_dati di stato della licenza DRM \_ \_ \_ vaghi        | Se impostato, potrebbero essere presenti più licenze valide per il contenuto.                                                                                         |
| \_OPL dati di stato della licenza DRM \_ \_ \_ \_ presenti | Se impostata, la licenza include i livelli di protezione dell'output (OPLs) che devono essere recuperati e controllati rispetto alla destinazione dell'output dell'applicazione. |
| \_ \_ \_ \_ SAP presente dati di stato delle licenze DRM \_ | Se impostato, il contenuto deve essere recapitato usando il percorso audio sicuro (SAP).                                                                                  |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene restituita (incapsulata in una struttura di [**\_ \_ \_ dati dello stato di licenza WM**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) ) da una chiamata a [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) quando si specifica una delle proprietà di stato della licenza DRM. Le proprietà sono riportate di seguito:

-   [**\_Riproduzione LICENSESTATE \_ DRM**](drm-licensestate-playback.md)
-   [**\_CopyToCD LICENSESTATE \_ DRM**](drm-licensestate-copytocd.md)
-   [**\_CopyToSDMIDevice LICENSESTATE \_ DRM**](drm-licensestate-copytosdmidevice.md)
-   [**\_CopyToNonSDMIDevice LICENSESTATE \_ DRM**](drm-licensestate-copytononsdmidevice.md)
-   [**\_CollaborativePlay LICENSESTATE \_ DRM**](drm-licensestate-collaborativeplay.md)
-   [**\_Copia di LICENSESTATE DRM \_**](drm-licensestate-copy.md)
-   [**\_PlaylistBurn LICENSESTATE \_ DRM**](drm-licensestate-playlistburn.md)

Se **dwCategory** è **il \_ \_ \_ conteggio dello stato di licenza WM DRM \_ \_ da \_ fino a,** la matrice **DateTime** conterrà in genere due date, una data "from" e una data "until". È anche possibile specificare due coppie di date per creare licenze più complesse.

Gli elementi della matrice **dwCount** corrispondono agli intervalli di date o date specificati nella matrice **DateTime** . Se **dwCategory** è **il \_ \_ \_ conteggio dello stato di licenza WM DRM \_ \_ da \_ until** e **DateTime** contiene una coppia di date, **dwCount** conterrà un elemento. Se **DateTime** contiene due coppie di date (quattro elementi), **dwCount** deve contenere due elementi, uno per ogni coppia di date.

In alcuni casi, è possibile che agli utenti sia stata rilasciata più di una licenza per un file. Potrebbero ad esempio avere acquisito una licenza che consentiva cinque Play fino alla fine del mese e successivamente ha acquisito una seconda licenza per diritti illimitati. In tal caso, il \_ \_ flag di dati dello stato delle licenze DRM \_ \_ è impostato in **dwVague** ( `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` ) e il componente DRM utilizzerà un algoritmo per determinare il set di diritti più probabile applicato. Quando una licenza scade, il componente DRM esamina le licenze rimanenti e così via fino a quando tutte le licenze non saranno scadute.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                      |
| Versione<br/>                  | Windows Media Format 7 SDK o versioni successive dell'SDK<br/>                       |
| Intestazione<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

