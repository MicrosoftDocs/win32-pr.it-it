---
description: L'interfaccia IAMErrorLog fornisce un metodo di callback per la registrazione degli errori in DirectShow Editing Services (DES). DES non implementa questa interfaccia.
ms.assetid: d5366072-2de7-437c-b198-cbc4d8623c45
title: Interfaccia IAMErrorLog (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f2edd1d315cc7ae35bbc200209667d49d53392ce86a10b40a067182cd0621124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756461"
---
# <a name="iamerrorlog-interface"></a>Interfaccia IAMErrorLog

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

`IAMErrorLog`L'interfaccia fornisce un metodo di callback per la registrazione degli errori in DirectShow Editing [Services](directshow-editing-services.md) (DES).

DES non implementa questa interfaccia. Per eseguire la registrazione degli errori, implementare questa interfaccia nell'applicazione e chiamare [**IAMSetErrorLog::p ut \_ ErrorLog**](iamseterrorlog-put-errorlog.md) nella sequenza temporale. Se si verifica un errore durante il rendering del progetto, DES chiamerà il metodo [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) implementato dall'applicazione.

DES registra gli errori solo quando si esegue il rendering di un progetto usando [**l'interfaccia IRenderEngine.**](irenderengine.md) Ad esempio, se si salva un progetto come grafico DirectShow filtro (con estensione grf) e si riproduce il file del grafo, non è presente alcuna registrazione degli errori. Per altre informazioni sull'uso di questa interfaccia, vedere [Registrazione degli errori](logging-errors.md).

## <a name="members"></a>Membri

**L'interfaccia IAMErrorLog** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMErrorLog** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IAMErrorLog** include questi metodi.



| Metodo                                   | Descrizione               |
|:-----------------------------------------|:--------------------------|
| [**LogError**](iamerrorlog-logerror.md) | Registra un errore.<br/> |



 

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



 

 
