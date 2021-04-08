---
description: Il metodo EvictNode rimuove un sistema di computer da un cluster. Il nodo da rimuovere viene specificato come parametro per il metodo.
ms.assetid: 4691d536-ade3-4a02-bc28-e31ebaf5d9e4
ms.tgt_platform: multiple
title: Metodo EvictNode della classe CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.EvictNode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d68ddc1adc0af335dcf2d4139cf7c1f0a381d986
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748138"
---
# <a name="evictnode-method-of-the-cim_clusteringservice-class"></a>Metodo EvictNode della classe CIM \_ ClusteringService

Il metodo **EvictNode** rimuove un sistema di computer da un cluster. Il nodo da rimuovere viene specificato come parametro per il metodo.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 EvictNode(
  [in] CIM_ComputerSystem REF CS
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CS* \[ in\]
</dt> <dd>

Riferimento al sistema del computer da rimuovere dal cluster.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 (zero) se il sistema del computer viene eliminato correttamente, 1 (uno) se il metodo non è supportato e qualsiasi altro numero se si è verificato un errore.

## <a name="remarks"></a>Commenti

Questo metodo non è attualmente implementato da WMI. Per usare questo metodo, è necessario implementarlo nel proprio provider.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_CLUSTERINGSERVICE CIM**](evictnode-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[**\_CLUSTERINGSERVICE CIM**](cim-clusteringservice.md)
</dt> </dl>

 

