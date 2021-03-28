---
description: Determina il percorso di una risorsa con il tipo e il nome specificati nel modulo specificato.
ms.assetid: d8322430-5064-407e-8b89-b86b75bf139e
title: FindResourceWrapW (funzione)
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
ms.openlocfilehash: 8f76d516570725fe6da5e8a21ec5a29699276ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227452"
---
# <a name="findresourcewrapw-function"></a>FindResourceWrapW (funzione)

\[**FindResourceWrapW** è disponibile per l'utilizzo in Windows XP. Potrebbe non essere disponibile nelle versioni successive. Usare invece [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) .\]

Determina il percorso di una risorsa con il tipo e il nome specificati nel modulo specificato.

> [!Note]  
> **FindResourceWrapW** è un wrapper per la funzione **FindResourceW** . Per ulteriori note sull'utilizzo, vedere [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) .

 

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

*hmodule* \[ in\]
</dt> <dd>

Tipo: **hmodule**

Handle per il modulo il cui file eseguibile contiene la risorsa. Il valore **null** specifica l'handle del modulo associato al file di immagine utilizzato dal sistema operativo per creare il processo corrente.

</dd> <dt>

*lpName* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Nome della risorsa. Per ulteriori informazioni, vedere [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).

</dd> <dt>

*lpType* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a una stringa che specifica il tipo di risorsa. Per ulteriori informazioni, vedere [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRSRC**

Se la funzione ha esito positivo, il valore restituito è un handle per il blocco di informazioni della risorsa specificata. Per ottenere un handle per la risorsa, passare questo handle alla funzione [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .

Se la funzione ha esito negativo, il valore restituito è **null**. Per ottenere informazioni estese sull'errore, chiamare la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Commenti

Se è necessario specificare una particolare localizzazione, utilizzare la funzione [**FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) anziché **FindResourceWrapW**.

**FindResourceWrapW** offre la possibilità di usare stringhe Unicode nei sistemi operativi precedenti. Il metodo preferito consiste nell'usare [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) insieme a Microsoft Layer for Unicode (MSLU).

**FindResourceWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 66.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Nessuno</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versione 5,0 o successiva)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **FindResourceWrapW** (Unicode)<br/>                                                                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea)
</dt> </dl>

 

 
