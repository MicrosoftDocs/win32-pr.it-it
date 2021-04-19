---
description: L'interfaccia IAMErrorLog fornisce un metodo di callback per la registrazione degli errori in DirectShow editing Services (DES). DES non implementa questa interfaccia.
ms.assetid: d5366072-2de7-437c-b198-cbc4d8623c45
title: Interfaccia IAMErrorLog (qedit. h)
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
ms.openlocfilehash: 48a1515ebf3e7c829a3e23772f1f84ee76c36ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326821"
---
# <a name="iamerrorlog-interface"></a>Interfaccia IAMErrorLog

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IAMErrorLog` interfaccia fornisce un metodo di callback per la registrazione degli errori in [DirectShow editing Services](directshow-editing-services.md) (des).

DES non implementa questa interfaccia. Per eseguire la registrazione degli errori, implementare questa interfaccia nell'applicazione e chiamare [**IAMSetErrorLog::p \_ log**](iamseterrorlog-put-errorlog.md) degli errori UT nella sequenza temporale. Se si verifica un errore quando si esegue il rendering del progetto, DES chiamerà il metodo [**IAMErrorLog:: LogError**](iamerrorlog-logerror.md) implementato dall'applicazione.

DES registra gli errori solo quando si esegue il rendering di un progetto usando l'interfaccia [**IRenderEngine**](irenderengine.md) . Se, ad esempio, si salva un progetto come un grafico del filtro DirectShow (formato. GRF) e si riproduce il file del grafo, non viene eseguita alcuna registrazione degli errori. Per ulteriori informazioni sull'utilizzo di questa interfaccia, vedere [registrazione degli errori](logging-errors.md).

## <a name="members"></a>Membri

L'interfaccia **IAMErrorLog** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMErrorLog** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAMErrorLog** dispone di questi metodi.



| Metodo                                   | Descrizione               |
|:-----------------------------------------|:--------------------------|
| [**LogError**](iamerrorlog-logerror.md) | Registra un errore.<br/> |



 

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



 

 
