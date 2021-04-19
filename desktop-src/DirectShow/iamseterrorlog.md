---
description: L'interfaccia IAMSetErrorLog imposta o recupera un log degli errori in servizi di modifica DirectShow (DES).
ms.assetid: ce658533-eacf-4b5d-9910-dca918de09e7
title: Interfaccia IAMSetErrorLog (qedit. h)
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
ms.openlocfilehash: c0a24d29625bf08bc2f4c728a61f5188e8bec211
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326809"
---
# <a name="iamseterrorlog-interface"></a>Interfaccia IAMSetErrorLog

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IAMSetErrorLog` interfaccia imposta o recupera un log degli errori in [servizi di modifica DirectShow](directshow-editing-services.md) (des). L'oggetto sequenza temporale implementa questa interfaccia. Le applicazioni possono utilizzare questa interfaccia per registrare gli errori di rendering in fase di esecuzione. Implementare l'interfaccia [**IAMErrorLog**](iamerrorlog.md) nell'applicazione, quindi chiamare il metodo [**IAMSetErrorLog::p log degli \_ errori UT**](iamseterrorlog-put-errorlog.md) nella sequenza temporale.

Per ulteriori informazioni sull'utilizzo di questa interfaccia, vedere [registrazione degli errori](logging-errors.md).

## <a name="members"></a>Membri

L'interfaccia **IAMSetErrorLog** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMSetErrorLog** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAMSetErrorLog** dispone di questi metodi.



| Metodo                                               | Descrizione                                                 |
|:-----------------------------------------------------|:------------------------------------------------------------|
| [**Ottieni \_ log degli errori**](iamseterrorlog-get-errorlog.md) | Recupera il log degli errori corrente per questo oggetto.<br/> |
| [**Inserisci \_ log degli errori**](iamseterrorlog-put-errorlog.md) | Specifica un log degli errori per l'oggetto.<br/>           |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
