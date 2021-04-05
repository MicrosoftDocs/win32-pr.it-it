---
description: La funzione EnumMonitors recupera informazioni sui monitoraggi di porta installati nel server specificato.
ms.assetid: 4d4fbed2-193f-426c-8463-eeb6b1eaf316
title: Funzione EnumMonitors (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMonitors
- EnumMonitorsA
- EnumMonitorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 1154cae0864b9d034ff356657d689cd3a768186f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756401"
---
# <a name="enummonitors-function"></a>EnumMonitors (funzione)

La funzione **EnumMonitors** recupera informazioni sui monitoraggi di porta installati nel server specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL EnumMonitors(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pMonitors,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del server in cui risiedono i monitoraggi. Se questo parametro è **null**, vengono enumerati i monitoraggi locali.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Versione della struttura a cui punta *pMonitors*.

Questo valore può essere 1 o 2.

</dd> <dt>

*pMonitors* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve una matrice di strutture. Il buffer deve essere sufficientemente grande da archiviare le stringhe a cui fanno riferimento i membri della struttura.

Per determinare le dimensioni del buffer richieste, chiamare **EnumMonitors** con *cbBuf* impostato su zero. **EnumMonitors** ha esito negativo, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ buffer insufficiente \_ e il parametro *pcbNeeded* restituisce la dimensione, in byte, del buffer necessario per memorizzare la matrice di strutture e i relativi dati.

Il buffer riceve una matrice di strutture di [**monitoraggio \_ info \_ 1**](monitor-info-1.md) se *Level* è 1 o [**monitora le strutture \_ info \_ 2**](monitor-info-2.md) se *Level* è 2.

</dd> <dt>

*cbBuf* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pMonitors*.

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di byte copiati se la funzione ha esito positivo o il numero di byte necessari se *cbBuf* è troppo piccolo.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di strutture restituite nel buffer a cui punta *pMonitors*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **EnumMonitorsW** (Unicode) e **EnumMonitorsA** (ANSI)<br/>                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Informazioni di monitoraggio \_ \_ 1**](monitor-info-1.md)
</dt> <dt>

[**Informazioni sul monitoraggio \_ \_ 2**](monitor-info-2.md)
</dt> </dl>

 

