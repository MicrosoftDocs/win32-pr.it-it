---
description: La funzione EnumPorts enumera le porte disponibili per la stampa in un server specificato.
ms.assetid: 72ea0e35-bf26-4c12-9451-8f6941990d82
title: Funzione EnumPorts (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPorts
- EnumPortsA
- EnumPortsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 2f4cceb6b6915f92139d8919b74f62ba4392381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314996"
---
# <a name="enumports-function"></a>EnumPorts (funzione)

La funzione **EnumPorts** enumera le porte disponibili per la stampa in un server specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL EnumPorts(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPorts,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del server di cui si desidera enumerare le porte di stampa.

Se *pname* è **null**, la funzione enumera le porte della stampante del computer locale.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Tipo di informazioni restituite nel buffer di *pPorts* . Se *Level* è 1, *pPorts* riceve una matrice di strutture di [**Port \_ info \_ 1**](port-info-1.md) . Se *Level* è 2, *pPorts* riceve una matrice di strutture [**Port \_ info \_ 2**](port-info-2.md) .

</dd> <dt>

*pPorts* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve una matrice di strutture delle informazioni di porta [**\_ \_ 1**](port-info-1.md) o della [**porta \_ \_ 2**](port-info-2.md) . Ogni struttura contiene dati che descrivono una porta stampante disponibile. Il buffer deve essere sufficientemente grande da archiviare le stringhe a cui puntano i membri della struttura.

Per determinare le dimensioni del buffer richieste, chiamare **EnumPorts** con *cbBuf* impostato su zero. **EnumPorts** ha esito negativo, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ buffer insufficiente \_ e il parametro *pcbNeeded* restituisce la dimensione, in byte, del buffer necessario per memorizzare la matrice di strutture e i relativi dati.

</dd> <dt>

*cbBuf* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pPorts*.

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di byte copiati nel buffer di *pPorts* . Se il buffer è troppo piccolo, la funzione ha esito negativo e la variabile riceve il numero di byte necessari.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di strutture [**Port \_ info \_ 1**](port-info-1.md) o [**Port \_ info \_ 2**](port-info-2.md) restituite nel buffer *pPorts* . Il numero di porte della stampante disponibili sul server specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

La funzione **EnumPorts** può avere esito positivo anche se per il server specificato da *pname* non è stata definita una stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **EnumPortsW** (Unicode) e **EnumPortsA** (ANSI)<br/>                                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPort**](addport.md)
</dt> <dt>

[**DeletePort**](deleteport.md)
</dt> <dt>

[**\_Informazioni porta \_ 1**](port-info-1.md)
</dt> <dt>

[**Informazioni sulla porta \_ \_ 2**](port-info-2.md)
</dt> </dl>

 

