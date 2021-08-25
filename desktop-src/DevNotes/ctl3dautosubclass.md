---
description: Crea automaticamente una sottoclasse e aggiunge effetti 3D a tutte le finestre di dialogo nell'applicazione.
ms.assetid: 96555052-c564-4cc7-9b24-e527f8e2f879
title: Funzione Ctl3dAutoSubclass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 5edc8bafb00d5444f18b61e0600fb075b6a7367c315c2ab1cfe38f911e9a84d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654611"
---
# <a name="ctl3dautosubclass-function"></a>Funzione Ctl3dAutoSubclass

Crea automaticamente una sottoclasse e aggiunge effetti 3D a tutte le finestre di dialogo nell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
PUBLIC BOOL FAR PASCAL Ctl3dAutoSubclass(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hinstApp* 
</dt> <dd>

Handle per l'applicazione da registrare come client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** a meno che non esista una delle condizioni seguenti, nel qual caso restituisce **FALSE**:

-   CTL3D è in esecuzione Windows versione 3.0 o precedente.
-   CTL3D non dispone di spazio disponibile nelle tabelle per l'applicazione corrente. CTL3D può essere in grado di eseguire contemporaneamente fino a 32 applicazioni.
-   CTL3D non è in grado di installare il relativo hook CBT.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
