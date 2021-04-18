---
description: La funzione InetGetAutodial restituisce le impostazioni di Autodial dal registro di sistema.
ms.assetid: e36761da-c050-4844-ad94-efdc77702f6f
title: InetGetAutodial (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InetGetAutodial
api_type:
- DllExport
api_location:
- Inetcfg.dll
ms.openlocfilehash: 15267cd00940f0386c8a5d9c0c54b070f2cff509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331192"
---
# <a name="inetgetautodial-function"></a>InetGetAutodial (funzione)

\[Questa funzione non è supportata e può essere modificata o non disponibile nelle versioni future di Windows. \]

La funzione **InetGetAutodial** restituisce le impostazioni di Autodial dal registro di sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InetGetAutodial(
  _Out_ LPBOOL lpfEnable,
  _Out_ LPSTR  lpszEntryName,
  _In_  DWORD  cbEntryNameSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpfEnable* \[ out\]
</dt> <dd>

Indica se la connessione automatica è abilitata. Il valore **true** al ritorno indica che la connessione automatica è abilitata.

</dd> <dt>

*lpszEntryName* \[ out\]
</dt> <dd>

Nell'output restituito è contenuto il nome della voce della rubrica impostata per la selezione automatica.

</dd> <dt>

*cbEntryNameSize* \[ in\]
</dt> <dd>

Dimensione del buffer allocato dal chiamante per il nome della voce della rubrica telefonica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione può restituire uno di questi valori.



| Codice restituito                                                                                                | Descrizione                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ riuscito**</dt> </dl>              | La chiamata è stata completata correttamente.<br/>                                                                                                                       |
| <dl> <dt>**ERRORI \_ argomenti non validi \_**</dt> </dl>       | *lpfEnable* o *lpszEntryName* contiene un puntatore **null** oppure il valore di *cbEntryNameSize* è zero.<br/>                                         |
| <dl> <dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt> </dl>  | Memoria insufficiente per l'allocazione di buffer interni.<br/>                                                                                    |
| <dl> <dt>**ERRORE \_ buffer insufficiente \_**</dt> </dl> | *cbEntryNameSize* non indica che il buffer a cui punta *lpszEntryName* è sufficientemente grande da ricevere il nome della voce della rubrica telefonica.<br/> |



 

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Inetcfg.dll</dt> </dl> |



 

 
