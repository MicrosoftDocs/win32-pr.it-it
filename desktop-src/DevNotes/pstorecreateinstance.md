---
description: Recupera un puntatore a interfaccia a un provider di archiviazione.
ms.assetid: 22b5b003-82fa-48f1-96db-a8d6dd70d6d1
title: Funzione PStoreCreateInstance (PStore. h)
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
ms.openlocfilehash: ce61a0d320b34ad09f4801d4ee5b53625e61501b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329166"
---
# <a name="pstorecreateinstance-function"></a>PStoreCreateInstance (funzione)

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

\[Questa funzione può essere modificata o non disponibile nelle versioni future di Windows. Usare le funzioni **CryptProtectData** e **CryptUnprotectData** anziché questa funzione.\]

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

*ppProvider* \[ out\]
</dt> <dd>

Puntatore al puntatore a interfaccia recuperato per il provider di archiviazione. Al termine dell'utilizzo dell'interfaccia, decrementare il conteggio dei riferimenti chiamando il relativo metodo [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) . Questo parametro non può essere **null**.

</dd> <dt>

*pProviderID* \[ in\]
</dt> <dd>

Puntatore al **GUID** che identifica il provider di archiviazione. Se questo parametro è **null**, viene utilizzato il provider di archiviazione di base.

</dd> <dt>

*mantenuta* \[ in\]
</dt> <dd>

Riservati deve essere **null**.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Riservati deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **HRESULT**. Il valore **S \_ OK** indica che la funzione ha avuto esito positivo.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata)
</dt> <dt>

[**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)
</dt> </dl>

 

 
