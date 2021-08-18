---
description: L'interfaccia IAMSetErrorLog imposta o recupera un log degli errori in DirectShow Editing Services (DES).
ms.assetid: ce658533-eacf-4b5d-9910-dca918de09e7
title: Interfaccia IAMSetErrorLog (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8a16e56de7f350b30c1b92c0c94ff3e3e06afc31b363c0b3a6e98017ce483aec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756401"
---
# <a name="iamseterrorlog-interface"></a>Interfaccia IAMSetErrorLog

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

`IAMSetErrorLog`L'interfaccia imposta o recupera un log degli errori in DirectShow Editing [Services](directshow-editing-services.md) (DES). L'oggetto sequenza temporale implementa questa interfaccia. Le applicazioni possono usare questa interfaccia per registrare gli errori di rendering in fase di esecuzione. Implementare [**l'interfaccia IAMErrorLog**](iamerrorlog.md) nell'applicazione e quindi chiamare il metodo [**IAMSetErrorLog::p ut \_ ErrorLog**](iamseterrorlog-put-errorlog.md) nella sequenza temporale.

Per altre informazioni sull'uso di questa interfaccia, vedere [Registrazione degli errori](logging-errors.md).

## <a name="members"></a>Membri

**L'interfaccia IAMSetErrorLog** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMSetErrorLog** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IAMSetErrorLog.**



| Metodo                                               | Descrizione                                                 |
|:-----------------------------------------------------|:------------------------------------------------------------|
| [**get \_ ErrorLog**](iamseterrorlog-get-errorlog.md) | Recupera il log degli errori corrente per questo oggetto .<br/> |
| [**put \_ ErrorLog**](iamseterrorlog-put-errorlog.md) | Specifica un log degli errori per l'oggetto .<br/>           |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
