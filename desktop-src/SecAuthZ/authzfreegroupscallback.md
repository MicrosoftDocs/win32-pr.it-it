---
description: Funzione definita dall'applicazione che libera la memoria allocata dalla funzione AuthzComputeGroupsCallback. AuthzFreeGroupsCallback è un segnaposto per il nome della funzione definita dall'applicazione.
ms.assetid: 5563311c-2bd1-4e96-ba0a-5a4225050f77
title: Funzione di callback AuthzFreeGroupsCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7d8942acbc67f122ea79f0b9e98793628b5f21f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760826"
---
# <a name="authzfreegroupscallback-callback-function"></a>Funzione di callback AuthzFreeGroupsCallback

La funzione **AuthzFreeGroupsCallback** è una funzione definita dall'applicazione che libera la memoria allocata dalla funzione [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md) . **AuthzFreeGroupsCallback** è un segnaposto per il nome della funzione definita dall'applicazione.

## <a name="syntax"></a>Sintassi


```C++
void CALLBACK AuthzFreeGroupsCallback(
  _In_ PSID_AND_ATTRIBUTES pSidAttrArray
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSidAttrArray* \[ in\]
</dt> <dd>

Puntatore alla memoria allocata da [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione di callback non restituisce un valore.

## <a name="remarks"></a>Commenti

Le variabili di attributo devono essere sotto forma di espressione se utilizzate con operatori logici; in caso contrario, vengono valutati come sconosciuti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                   |
| Componente ridistribuibile<br/>          | Windows Server 2003 Administration Tools Pack in Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di controllo di accesso di base](authorization-functions.md)
</dt> <dt>

[**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md)
</dt> </dl>

 

 




