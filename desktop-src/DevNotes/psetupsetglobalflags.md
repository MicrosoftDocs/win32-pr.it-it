---
description: Disabilita le funzionalità.
ms.assetid: 2ea2dcfb-84e6-4f83-9afd-c3050b53f37c
title: Funzione pSetupSetGlobalFlags
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupSetGlobalFlags
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: d28bb948d351b2b9ad54c7e2bdc8c8cbfde83f6f4ade42a0f90440eca28bfc05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955700"
---
# <a name="psetupsetglobalflags-function"></a>Funzione pSetupSetGlobalFlags

\[Questa funzione non è disponibile in Windows Vista o Windows Server 2008.\]

Disabilita le funzionalità.

## <a name="syntax"></a>Sintassi


```C++
VOID pSetupSetGlobalFlags(
  _In_ DWORD Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Valore* \[ Pollici\]
</dt> <dd>

Flag utilizzati per disabilitare l'interfaccia utente o il backup automatico.



| Valore                                                                                                                                                                                                                                         | Significato                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PSPGF_NONINTERACTIVE"></span><span id="pspgf_noninteractive"></span><dl> <dt>**PSPGF \_ NonINTERACTIVE**</dt> <dt>0x004</dt> </dl> | Impostare per disabilitare l'interfaccia utente.<br/>   |
| <span id="PSPGF_NO_BACKUP"></span><span id="pspgf_no_backup"></span><dl> <dt>**PSPGF \_ NO \_ BACKUP**</dt> <dt>0x002</dt> </dl>               | Impostare per disabilitare il backup automatico.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
