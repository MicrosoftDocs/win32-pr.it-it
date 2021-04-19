---
description: La funzione ShowJavaConsole è un supporto per il debug di sviluppatori Java. Gli applet (o altro codice Java) in esecuzione in Internet Explorer possono utilizzarlo per visualizzare i messaggi di errore e altre informazioni.
ms.assetid: 070dd833-f8cc-403e-afbf-325648760d5f
title: ShowJavaConsole (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- extern
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 522885bfdd07843549375977630d8d1a7c6776f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328176"
---
# <a name="showjavaconsole-function"></a>ShowJavaConsole (funzione)

La funzione **ShowJavaConsole** è un supporto per il debug di sviluppatori Java. Gli applet (o altro codice Java) in esecuzione in Internet Explorer possono utilizzarlo per visualizzare i messaggi di errore e altre informazioni.

## <a name="syntax"></a>Sintassi


```C++
void extern ShowJavaConsole(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

<dl></dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La chiamata di **ShowJavaConsole** fa sì che la macchina virtuale Java (VM) visualizzi la finestra della console Java. La finestra della console Java può visualizzare l'output del debug dal codice Java in esecuzione nel processo chiamante. Questa operazione viene in genere usata solo da un'applicazione che ospita la macchina virtuale Java. Esiste una sola finestra della console Java per ogni processo; per più chiamate all'API si ottiene la visualizzazione della stessa finestra. In altre parole, se la finestra della console è già visualizzata, non viene eseguita alcuna operazione; Se la finestra non è stata visualizzata o l'utente lo ha chiuso, viene visualizzata la finestra.

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
