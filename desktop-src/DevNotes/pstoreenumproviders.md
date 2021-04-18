---
description: Ottiene un oggetto enumeratore che può essere utilizzato a sua volta per enumerare i provider di archiviazione protetti attualmente installati nel sistema.
ms.assetid: df162086-caeb-427f-9db8-9722855cfbbf
title: Funzione PStoreEnumProviders (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreEnumProviders
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: f4f97bdae8646d3a4d683bb5b87bf72efb4c5a5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330961"
---
# <a name="pstoreenumproviders-function"></a>PStoreEnumProviders (funzione)

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Ottiene un oggetto enumeratore che può essere utilizzato a sua volta per enumerare i provider di archiviazione protetti attualmente installati nel sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PStoreEnumProviders(
   DWORD                dwFlags,
   IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere zero.

</dd> <dt>

*ppenum* 
</dt> <dd>

Puntatore a un puntatore a un'interfaccia [**IEnumPStoreProviders**](ienumpstoreproviders.md) che può essere utilizzata per enumerare i provider installati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce un valore **HRESULT**.

## <a name="remarks"></a>Commenti

Il componente di archiviazione protetta dispone di un'architettura basata su provider. Le applicazioni che usano l'archiviazione protetta possono specificare quali provider installati usare durante l'archiviazione e il recupero dei dati.

La funzione **PStoreEnumProviders** viene utilizzata per enumerare i provider di archiviazione protetti installati. Ogni provider viene identificato da un identificatore univoco globale (GUID).

Fino a questo momento, è già stato scritto un solo provider di archiviazione protetto. Dato che il servizio di archiviazione protetto è attualmente deprecato, è molto improbabile che vengano generati altri provider. Di conseguenza, questa funzione non deve essere usata per alcuno scopo.

A questa funzione non è associata alcuna libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumPStoreProviders**](ienumpstoreproviders.md)
</dt> </dl>

 

 
