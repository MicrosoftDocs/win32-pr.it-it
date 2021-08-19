---
description: Determina la posizione di una risorsa con il tipo e il nome specificati nel modulo specificato.
ms.assetid: d8322430-5064-407e-8b89-b86b75bf139e
title: Funzione FindResourceWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindResourceWrapW
- FindResourceWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: bfd640aaf0bbc68e8798f62f41542d794db34808674c0bdb47587c7396ad7bc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094196"
---
# <a name="findresourcewrapw-function"></a>Funzione FindResourceWrapW

\[**FindResourceWrapW** è disponibile per l'uso in Windows XP. Potrebbe non essere disponibile nelle versioni successive. In alternativa, [**è consigliabile usare FindResourceW.**](/windows/win32/api/winbase/nf-winbase-findresourcea)\]

Determina la posizione di una risorsa con il tipo e il nome specificati nel modulo specificato.

> [!Note]  
> **FindResourceWrapW** è un wrapper per la **funzione FindResourceW.** Per altre note sull'utilizzo, vedere [**FindResource.**](/windows/win32/api/winbase/nf-winbase-findresourcea)

 

## <a name="syntax"></a>Sintassi


```C++
HRSRC FindResourceWrapW(
  _In_ HMODULE hModule,
  _In_ LPCWSTR lpName,
  _In_ LPCWSTR lpType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hModule* \[ Pollici\]
</dt> <dd>

Tipo: **HMODULE**

Handle per il modulo il cui file eseguibile contiene la risorsa. Il valore **NULL specifica** l'handle di modulo associato al file di immagine usato dal sistema operativo per creare il processo corrente.

</dd> <dt>

*lpName* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Nome della risorsa. Per altre informazioni, vedere [**FindResource.**](/windows/win32/api/winbase/nf-winbase-findresourcea)

</dd> <dt>

*lpType* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a una stringa che specifica il tipo di risorsa. Per altre informazioni, vedere [**FindResource.**](/windows/win32/api/winbase/nf-winbase-findresourcea)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRSRC**

Se la funzione ha esito positivo, il valore restituito è un handle per il blocco di informazioni della risorsa specificata. Per ottenere un handle per la risorsa, passare questo handle alla [**funzione LoadResource.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)

Se la funzione ha esito negativo, il valore restituito è **NULL.** Per ottenere informazioni estese sull'errore, chiamare [**la funzione GetLastError.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Commenti

Se è necessario specificare una particolare localizzazione, usare la [**funzione FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) anziché **FindResourceWrapW.**

**FindResourceWrapW** offre la possibilità di usare stringhe Unicode nei sistemi operativi precedenti. Il metodo preferito è usare [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) insieme a Microsoft Layer for Unicode (MSLU).

**FindResourceWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 66.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Nessuno</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versione 5.0 o successiva)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **FindResourceWrapW** (Unicode)<br/>                                                                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Findresource**](/windows/win32/api/winbase/nf-winbase-findresourcea)
</dt> </dl>

 

 
