---
description: Apre un volume specificato e inizializza il relativo oggetto di controllo della quota.
ms.assetid: 20eae2a3-f602-48a2-bf1c-65570e7a5d21
title: Metodo tialize DiskQuotaControl.Ini
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
ms.openlocfilehash: 919720f01c67b6df3189b760aa8cefbb29615179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977175"
---
# <a name="diskquotacontrolinitialize-method"></a>Metodo tialize DiskQuotaControl.Ini

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

Tipo: **stringa**

Valore stringa che contiene il percorso completo del volume da inizializzare.

</dd> <dt>

*bReadWrite* 
</dt> <dd>

Tipo: **booleano**

Valore booleano che specifica la modalità di apertura del volume. Impostare *bReadWrite* su **true** per l'accesso in lettura/scrittura o **false** per l'accesso in sola lettura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




