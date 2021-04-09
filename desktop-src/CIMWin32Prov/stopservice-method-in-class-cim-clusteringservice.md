---
description: Arresta il servizio rappresentato dall'oggetto derivato da CIM \_ ClusteringService.
ms.assetid: b8dbaeeb-819b-469b-9f5e-d658e88d1a6e
ms.tgt_platform: multiple
title: Metodo StopService della classe CIM_ClusteringService (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3a55f7b0a9527092e51156d55c7513ee59c4861
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877833"
---
# <a name="stopservice-method-of-the-cim_clusteringservice-class"></a>Metodo StopService della classe CIM \_ ClusteringService

Il metodo **StopService** arresta il servizio rappresentato dall'oggetto derivato da [**CIM \_ ClusteringService**](cim-clusteringservice.md). Questo metodo viene ereditato dal [**\_ servizio CIM**](cim-service.md).

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) se il servizio è stato arrestato correttamente, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.

## <a name="remarks"></a>Commenti

Questo metodo non è attualmente implementato da WMI. Per usare questo metodo, è necessario implementarlo nel proprio provider.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| Intestazione<br/>                   | <dl> <dt>Sdoias. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_CLUSTERINGSERVICE CIM**](stopservice-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[**\_CLUSTERINGSERVICE CIM**](cim-clusteringservice.md)
</dt> </dl>

 

