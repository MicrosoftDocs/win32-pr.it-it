---
title: Evento ConnectionStatusChanged
description: Si verifica quando cambia lo stato della connessione di rete del dispositivo.
ms.assetid: d1f04fa5-895e-4e86-9643-e880388dcded
keywords:
- API di streaming multimediale per gli eventi ConnectionStatusChanged
topic_type:
- apiref
api_name:
- ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8034cf49298b6523667f2434324a5be9da3b639
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726762"
---
# <a name="connectionstatuschanged-event"></a>Evento ConnectionStatusChanged

Si verifica quando cambia lo stato della connessione di rete del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
void ConnectionStatusChanged();
```



## <a name="parameters"></a>Parametri

Questo evento non contiene parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Per gestire le notifiche da questo evento, registrare una funzione del gestore eventi [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) usando il metodo [**Add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) . Per annullare la registrazione del gestore eventi, usare il metodo [**Remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) .

 

 