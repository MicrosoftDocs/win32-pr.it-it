---
title: Struttura WINBIO_BSP_SCHEMA ( \_ tipi WINBIO. h)
description: Descrive le funzionalità di un provider di servizi biometrico.
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
keywords:
- Struttura di WINBIO_BSP_SCHEMA Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_BSP_SCHEMA
topic_type:
- apiref
api_name:
- WINBIO_BSP_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ae63aefb64eb22f454559b76e9922242ca9530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476876"
---
# <a name="winbio_bsp_schema-structure"></a>\_ \_ Struttura dello schema BSP WINBIO

La **struttura \_ \_ dello schema BSP WINBIO** descrive le funzionalità di un provider di servizi biometrico. Questa struttura viene utilizzata dalla funzione [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_BSP_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           BspId;
  WINBIO_STRING         Description;
  WINBIO_STRING         Vendor;
  WINBIO_VERSION        Version;
} WINBIO_BSP_SCHEMA, *PWINBIO_BSP_SCHEMA;
```



## <a name="members"></a>Members

<dl> <dt>

**BiometricFactor**
</dt> <dd>

Tipo di misurazione biometrica usata dal dispositivo. Attualmente deve essere **WINBIO \_ \_ impronta digitale del tipo**.

</dd> <dt>

**BspId**
</dt> <dd>

Valore che identifica in modo univoco questo componente del provider di servizi biometrico.

</dd> <dt>

**Descrizione**
</dt> <dd>

Stringa Unicode con terminazione **null** che contiene una descrizione del provider di servizi biometrici.

</dd> <dt>

**Fornitore**
</dt> <dd>

Stringa Unicode con terminazione **null** che contiene il nome del fornitore che fornisce il provider di servizi biometrico.

</dd> <dt>

**Versione**
</dt> <dd>

Struttura [**di \_ versione di WINBIO**](winbio-version.md) che contiene la versione software del componente provider di servizi biometrico.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture delle applicazioni client](client-application-structures.md)
</dt> <dt>

[**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 





