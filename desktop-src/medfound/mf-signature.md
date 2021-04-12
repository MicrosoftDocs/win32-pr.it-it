---
description: Contiene una firma dell'elenco di revoche globale (GRL).
ms.assetid: 388a901c-6202-41cf-9c3d-f29d8ccca76b
title: Struttura MF_SIGNATURE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_SIGNATURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4827fea8e4259609cbb54f2b58a3d1c88ad6c23e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233621"
---
# <a name="mf_signature-structure"></a>\_Struttura della firma MF

Contiene una firma dell'elenco di revoche globale (GRL).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _MF_SIGNATURE {
  DWORD dwSignVer;
  DWORD cbSign;
  BYTE  rgSign[1];
} MF_SIGNATURE;
```



## <a name="members"></a>Members

<dl> <dt>

**dwSignVer**
</dt> <dd>

Numero di versione della firma.

</dd> <dt>

**cbSign**
</dt> <dd>

Dimensioni in byte della firma.

</dd> <dt>

**rgSign**
</dt> <dd>

Matrice di byte di dimensioni **cbSign** che contiene la firma. La dimensione effettiva della matrice è maggiore delle dimensioni specificate nella dichiarazione della struttura.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura non è dichiarata in un'intestazione SDK. Per usare questa struttura, aggiungere la dichiarazione mostrata qui al codice sorgente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Revoca del certificato OPM](opm-certificate-revocation.md)
</dt> <dt>

[Strutture OPM](opm-structures.md)
</dt> </dl>

 

 




