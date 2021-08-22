---
description: La funzione ShowJavaConsole è un supporto per il debug per sviluppatori Java. Le applet (o altro codice Java) in Internet Explorer possono usarle per visualizzare messaggi di errore e altre informazioni.
ms.assetid: 070dd833-f8cc-403e-afbf-325648760d5f
title: Funzione ShowJavaConsole
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
ms.openlocfilehash: 0a8517d32057b6434d3822cc02977f6afd72c1b387b78e85e53810bd27f00550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075855"
---
# <a name="showjavaconsole-function"></a>Funzione ShowJavaConsole

La **funzione ShowJavaConsole** è un supporto per il debug per sviluppatori Java. Le applet (o altro codice Java) in Internet Explorer possono usarle per visualizzare messaggi di errore e altre informazioni.

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

Se **si chiama ShowJavaConsole,** la macchina virtuale Java visualizza la finestra della console Java. La finestra della console Java stessa può visualizzare l'output di debug del codice Java in esecuzione nel processo chiamante. In genere, questa operazione viene usata solo da un'applicazione che ospita la macchina virtuale Java. Esiste una sola finestra della console Java per ogni processo. Più chiamate all'API comportano la visualizzazione della stessa finestra. In altre parole, se la finestra della console è già visualizzata, non accade nulla. se la finestra non è stata visualizzata o l'utente l'ha chiusa, viene visualizzata la finestra.

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
