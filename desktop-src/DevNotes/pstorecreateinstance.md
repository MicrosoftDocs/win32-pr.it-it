---
description: Recupera un puntatore a interfaccia a un provider di archiviazione.
ms.assetid: 22b5b003-82fa-48f1-96db-a8d6dd70d6d1
title: Funzione PStoreCreateInstance (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreCreateInstance
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: 2e32319e9585f5d1a80d0473c6ce27167f0ec181b81b974c526371b29c018b03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955690"
---
# <a name="pstorecreateinstance-function"></a>Funzione PStoreCreateInstance

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

\[Questa funzione può essere modificata o non disponibile nelle versioni future Windows. Usare le **funzioni CryptProtectData** e **CryptUnprotectData** anziché questa funzione.\]

Recupera un puntatore a interfaccia a un provider di archiviazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT __stdcall PStoreCreateInstance(
  _Out_ IPStore        **ppProvider,
  _In_  PST_PROVIDERID *pProviderID,
  _In_  void           *pReserved,
  _In_  DWORD          dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppProvider* \[ Cambio\]
</dt> <dd>

Puntatore al puntatore a interfaccia recuperato per il provider di archiviazione. Al termine dell'uso dell'interfaccia, decrementare il conteggio dei riferimenti chiamando il [**relativo metodo IUnknown::Release.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) Questo parametro non può essere **NULL.**

</dd> <dt>

*pProviderID* \[ Pollici\]
</dt> <dd>

Puntatore al **GUID che** identifica il provider di archiviazione. Se questo parametro è **NULL,** viene usato il provider di archiviazione di base.

</dd> <dt>

*pReserved* \[ Pollici\]
</dt> <dd>

Riservato; deve essere **NULL.**

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Riservato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **HRESULT.** Il valore **S \_ OK** indica che la funzione ha avuto esito positivo.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata)
</dt> <dt>

[**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)
</dt> </dl>

 

 
