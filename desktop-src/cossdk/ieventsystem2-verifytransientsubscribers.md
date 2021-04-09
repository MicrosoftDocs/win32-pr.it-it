---
description: Verifica l'esistenza di tutti i sottoscrittori temporanei nell'archivio dati. Chiamando questo metodo, è possibile verificare che tutti i sottoscrittori temporanei elencati nell'archivio dati siano attivi.
ms.assetid: fffdde33-e960-42ef-a089-8ea8a6f33d52
title: 'Metodo IEventSystem2:: VerifyTransientSubscribers'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.VerifyTransientSubscribers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4415f405b95f341b645ca1dccbf254df2ffc7167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966072"
---
# <a name="ieventsystem2verifytransientsubscribers-method"></a>Metodo IEventSystem2:: VerifyTransientSubscribers

Verifica l'esistenza di tutti i sottoscrittori temporanei nell'archivio dati. Chiamando questo metodo, è possibile verificare che tutti i sottoscrittori temporanei elencati nell'archivio dati siano attivi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT VerifyTransientSubscribers();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, e \_ OutOfMemory, e \_ imprevisto, e ha \_ esito negativo e S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEventSystem2**](ieventsystem2.md)
</dt> </dl>

 

 




