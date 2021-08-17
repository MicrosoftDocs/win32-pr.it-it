---
description: Il metodo IsPhysicalClearDisabled della classe Win32 Tpm indica se solo il proprietario del dispositivo può essere in grado di \_ cancellare il dispositivo.
ms.assetid: b87f1c4f-8735-45c5-9256-53dbb9579f95
title: Metodo IsPhysicalClearDisabled della Win32_Tpm classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 7fd8841ad48480434fa1a686c2349e82d94eb01eda4f52084fd579cf67784870
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891881"
---
# <a name="isphysicalcleardisabled-method-of-the-win32_tpm-class"></a>Metodo IsPhysicalClearDisabled della classe Tpm Win32 \_

Il **metodo IsPhysicalClearDisabled** della classe [**\_ Win32 Tpm**](win32-tpm.md) indica se solo il proprietario del dispositivo può essere in grado di cancellare il dispositivo.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsPhysicalClearDisabled(
  [out] boolean IsPhysicalClearDisabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsPhysicalClearDisabled* \[ Cambio\]
</dt> <dd>

Tipo: **booleano**

Se **true,** solo il proprietario del dispositivo è in grado di cancellare il dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi di base TPM.

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Questo valore viene reimpostato su **false** all'inizio di ogni ciclo di avvio.

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                      |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
