---
description: Ottiene le dimensioni di un certificato per un driver di visualizzazione.
ms.assetid: fd52e939-127a-4493-8406-31f7767921cd
title: GetCertificateSize (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateSize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: bcd1f49ce65978c6a89c89cee1fda38e41434065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342456"
---
# <a name="getcertificatesize-function"></a>GetCertificateSize (funzione)

> [!IMPORTANT]
> Questa funzione viene utilizzata da [Output Protection Manager](output-protection-manager.md) (OPM) per accedere alla funzionalità nel driver di visualizzazione. Le applicazioni non devono chiamare questa funzione.

 

Ottiene le dimensioni di un certificato per un driver di visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI GetCertificateSize(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ ULONG                    *pulCertificateLength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pstrDeviceName* \[ in\]
</dt> <dd>

Puntatore a una struttura [**di \_ stringhe Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .

</dd> <dt>

*ctPVPCertificateType* \[ in\]
</dt> <dd>

Tipo di certificato, specificato come membro dell'enumerazione del **tipo di \_ certificato \_ DXGKMDT** .

</dd> <dt>

*pulCertificateLength* \[ out\]
</dt> <dd>

Riceve le dimensioni in byte del certificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**. In caso contrario, restituisce un codice di errore **NTSTATUS** .

## <a name="remarks"></a>Commenti

Le applicazioni devono chiamare il metodo [**IOPMVideoOutput:: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) anziché questa funzione.

A questa funzione non è associata alcuna libreria di importazione. Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di OPM](opm-functions.md)
</dt> <dt>

[Gestione protezione output](output-protection-manager.md)
</dt> </dl>

 

 
