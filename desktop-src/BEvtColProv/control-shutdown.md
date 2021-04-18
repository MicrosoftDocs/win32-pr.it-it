---
description: Arresta l'agente di raccolta. Se l'agente di raccolta è in esecuzione come servizio, l'arresto del servizio è l'approccio migliore.
ms.assetid: fab3e060-156f-46f5-98a2-d47a23d64552
ms.tgt_platform: multiple
title: Metodo Shutdown della classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Shutdown
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d401ac528498d7b8ab5ccacbf6a0b5bf781555f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304449"
---
# <a name="shutdown-method-of-the-control-class"></a>Metodo Shutdown della classe Control

Arresta l'agente di raccolta. Se l'agente di raccolta è in esecuzione come servizio, l'arresto del servizio è l'approccio migliore.

## <a name="syntax"></a>Sintassi


```mof
void Shutdown();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                       |
| Spazio dei nomi<br/>                | Radice \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

 




