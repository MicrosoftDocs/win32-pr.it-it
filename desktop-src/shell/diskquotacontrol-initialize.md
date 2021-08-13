---
description: Apre un volume specificato e inizializza il relativo oggetto di controllo della quota.
ms.assetid: 20eae2a3-f602-48a2-bf1c-65570e7a5d21
title: DiskQuotaControl.Inimetodo tialize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.Initialize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0df879c626ccdac7494077f021c23a6e42b24f0df3aa780d1be8b1af8225527a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455901"
---
# <a name="diskquotacontrolinitialize-method"></a>DiskQuotaControl.Inimetodo tialize

Apre un volume specificato e inizializza il relativo oggetto di controllo della quota.

## <a name="syntax"></a>Sintassi


```JScript
DiskQuotaControl.Initialize(
  sPath,
  bReadWrite
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sPath* 
</dt> <dd>

Tipo: **Stringa**

Valore stringa che contiene il percorso completo del volume da inizializzare.

</dd> <dt>

*bReadWrite* 
</dt> <dd>

Tipo: **Boolean**

Valore booleano che specifica la modalità di apertura del volume. Impostare *bReadWrite su* **TRUE per** l'accesso in lettura/scrittura o **FALSE** per l'accesso in sola lettura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




