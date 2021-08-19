---
title: ConnectionStatusChanged - evento
description: Si verifica quando cambia lo stato della connessione di rete del dispositivo.
ms.assetid: d1f04fa5-895e-4e86-9643-e880388dcded
keywords:
- API Streaming multimediale dell'evento ConnectionStatusChanged
topic_type:
- apiref
api_name:
- ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ccc19c71b56977a77ac5ec05448ea72eaff79d9e96b42f4f297d7046079f571
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060431"
---
# <a name="connectionstatuschanged-event"></a>ConnectionStatusChanged - evento

Si verifica quando cambia lo stato della connessione di rete del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
void ConnectionStatusChanged();
```



## <a name="parameters"></a>Parametri

Questo evento non ha parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Per gestire le notifiche da questo evento, registrare [**una funzione del gestore dell'evento ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) usando il metodo add [**\_ ConnectionStatusChanged.**](ibasicdevice-add-connectionstatuschanged.md) Per annullare la registrazione del gestore eventi, usare [**il \_ metodo remove ConnectionStatusChanged.**](ibasicdevice-remove-connectionstatuschanged.md)

 

 