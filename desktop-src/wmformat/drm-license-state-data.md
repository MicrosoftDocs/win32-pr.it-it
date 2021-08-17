---
title: DRM_LICENSE_STATE_DATA struttura (Drmexternals.h)
description: La struttura DRM \_ LICENSE STATE DATA contiene informazioni sulle licenze relative a un diritto \_ \_ DRM specificato.
ms.assetid: 5ca577b5-d28b-4e36-8af7-6fae4300d464
keywords:
- DRM_LICENSE_STATE_DATA struttura windows Media Format
- struttura windows Media Format
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
ms.openlocfilehash: 3e6703481dc1d3608a8bf08ab2bbd216db4a9ecdc91bd4604d2b9de7d7de4fa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848534"
---
# <a name="drm_license_state_data-structure-drmexternalsh"></a>DRM_LICENSE_STATE_DATA struttura (Drmexternals.h)

La **struttura DRM \_ LICENSE STATE \_ \_ DATA** contiene [*informazioni sulle licenze*](wmformat-glossary.md) relative a un diritto [*DRM*](wmformat-glossary.md) specificato.

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

Categoria della stringa da visualizzare. Vedere [**DRM \_ LICENSE STATE \_ CATEGORY \_ per**](drm-license-state-category.md) i valori possibili e il relativo significato.

</dd> <dt>

**dwNumCounts**
</dt> <dd>

Numero di elementi forniti in **dwCount.** Questo valore è in genere 0 o 1.

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

Matrice di 0 o 1 o più **DWORD** che rappresentano il numero di volte in cui può essere eseguita l'azione specificata in **dwCategory.** Vedere la sezione Osservazioni.

</dd> <dt>

**dwNumDates**
</dt> <dd>

Numero di elementi forniti in **datetime.** In genere non vengono usate più di due date, ad esempio con una licenza valida da una data a un'altra.

</dd> <dt>

**datetime \[ 4\]**
</dt> <dd>

Matrice di una o più strutture FILETIME che rappresentano una o più date nella licenza. Il significato di una determinata data dipende dal valore di **dwCategory**.

</dd> <dt>

**dwVague**
</dt> <dd>

Zero o più dei flag seguenti combinati con un'operazione OR bit per **bit:**



| Flag                                    | Descrizione                                                                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| DRM \_ LICENSE STATE DATA \_ \_ -1000000000000 \_        | Se impostata, potrebbero essere presenti più licenze che si applicano al contenuto.                                                                                         |
| DRM \_ LICENSE \_ STATE \_ DATA \_ OPL \_ PRESENT | Se impostata, la licenza include i livelli di protezione dell'output (OPL) che devono essere recuperati e verificati rispetto alla destinazione dell'output dell'applicazione. |
| DRM \_ LICENSE \_ STATE \_ DATA \_ SAP \_ PRESENT | Se impostato, il contenuto deve essere recapitato usando un percorso audio sicuro (SAP).                                                                                  |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene restituita (incapsulata in una struttura [**WM \_ LICENSE STATE \_ \_ DATA)**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) da una chiamata a [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) quando si specifica una delle proprietà dello stato della licenza DRM. Le proprietà sono riportate di seguito:

-   [**Riproduzione dello stato di licenza DRM \_ \_**](drm-licensestate-playback.md)
-   [**DRM \_ LicenseState \_ CopyToCD**](drm-licensestate-copytocd.md)
-   [**DRM \_ LicenseState \_ CopyToSDMIDevice**](drm-licensestate-copytosdmidevice.md)
-   [**DRM \_ LicenseState \_ CopyToNonSDMIDevice**](drm-licensestate-copytononsdmidevice.md)
-   [**DRM \_ LicenseState \_ CollaborativePlay**](drm-licensestate-collaborativeplay.md)
-   [**DRM \_ LicenseState \_ Copy**](drm-licensestate-copy.md)
-   [**Playlist DRM \_ LicenseState Playlist (Playlist stato licenza \_ DRM)**](drm-licensestate-playlistburn.md)

Se **dwCategory è** **WM \_ DRM LICENSE STATE COUNT \_ \_ FROM \_ \_ \_ UNTIL,** la matrice **datetime** conterrà in genere due date, una data "from" e una data "until". È anche possibile specificare due coppie di date per creare licenze più complesse.

Gli elementi della matrice **dwCount** corrispondono alle date o agli intervalli di date specificati nella **matrice datetime.** Se **dwCategory è** **WM \_ DRM LICENSE STATE COUNT \_ \_ FROM \_ \_ \_ UNTIL** e **datetime** contiene una coppia di date, **dwCount** conterrà un elemento. Se **datetime** contiene due coppie di date (quattro elementi), **dwCount** deve contenere due elementi, uno per ogni coppia di date.

In alcuni casi, è possibile che agli utenti sia stata rilasciata più di una licenza per un file. Ad esempio, potrebbero aver acquisito una licenza che consentiva cinque giochi fino alla fine del mese e successivamente acquisito una seconda licenza per diritti illimitati. In tal caso, il flag DRM LICENSE STATE DATA ALGORITHM è impostato \_ \_ in \_ \_ **dwVague** ( ) e il componente `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` DRM userà un algoritmo per determinare il set più probabile di diritti applicati. Alla scadenza di una licenza, il componente DRM esaminerà le licenze rimanenti e così via fino alla scadenza di tutte le licenze.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                      |
| Versione<br/>                  | Windows Media Format 7 SDK o versioni successive dell'SDK<br/>                       |
| Intestazione<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

