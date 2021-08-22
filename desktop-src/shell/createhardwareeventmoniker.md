---
description: Crea un moniker che rappresenta un componente hardware e il gestore eventi associato. AutoPlay usa questa funzione per consentire alle applicazioni di usare gli eventi AutoPlay.
title: Funzione CreateHardwareEventMoniker
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHardwareEventMoniker
api_type:
- DllExport
api_location:
- Shsvcs.dll
ms.assetid: ff0ad023-42ea-4c74-adae-af55527b6ac3
ms.openlocfilehash: 42f2da51bac93733a74113d3a567802975aca18be2a34f6fa349ff65349749c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460555"
---
# <a name="createhardwareeventmoniker-function"></a>Funzione CreateHardwareEventMoniker

\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]

Crea un moniker che rappresenta un componente hardware e il gestore eventi associato. AutoPlay usa questa funzione per consentire alle applicazioni di usare gli eventi AutoPlay.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateHardwareEventMoniker(
  _In_  REFCLSID clsid,
  _In_  LPCTSTR  pszEventHandler,
  _Out_ IMoniker **ppmoniker
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*clsid* \[ Pollici\]
</dt> <dd>

Tipo: **REFCLSID**

ID della classe a cui viene associato il moniker.

</dd> <dt>

*pszEventHandler* \[ Pollici\]
</dt> <dd>

Tipo: **LPCTSTR**

Nome del gestore eventi.

</dd> <dt>

*ppmoniker* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***

Indirizzo di una variabile puntatore che riceve il puntatore a [**interfaccia IMoniker.**](/windows/win32/api/objidl/nn-objidl-imoniker)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Usare **CreateHardwareEventMoniker** durante la registrazione delle applicazioni in esecuzione in modo che tali applicazioni abbia accesso agli eventi AutoPlay. Per usare gli eventi AutoPlay nelle applicazioni in esecuzione, è innanzitutto necessario creare un nuovo componente che implementa [**l'interfaccia IHWEventHandler.**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) Inizializzare questa interfaccia con il valore InitCmdLine della voce del gestore specifico sotto la chiave **Handlers,** perché AutoPlay non chiama il [**metodo Initialize.**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize)

È necessario chiamare **CreateHardwareEventMoniker** per ottenere un moniker che rappresenta il componente e il relativo gestore eventi. Usare quindi il valore restituito nel *parametro ppmoniker* per registrare il componente nella tabella degli oggetti in esecuzione (ROT, Running Object Table), come illustrato nell'esempio.

Si noti **che CreateHardwareEventMoniker** non è definito in un file di intestazione. Per usarlo nel codice, è necessario ottenere un handle per il file Shsvcs.dll tramite una chiamata a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya). Usare quindi tale handle in una chiamata a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per ottenere un'istanza della **funzione CreateHardwareEventMoniker.**

La chiamata a [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) richiede l'immissione delle informazioni **AppID** seguenti nel Registro di sistema.

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Nessuno</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Shsvcs.dll</dt> </dl> |



 

 
