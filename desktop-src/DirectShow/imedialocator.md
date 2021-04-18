---
description: L'interfaccia IMediaLocator fornisce metodi per la convalida dei nomi di file nei servizi di modifica DirectShow (DES).
ms.assetid: 6c1ae957-a2be-454b-9451-772e4a670677
title: Interfaccia IMediaLocator (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9664bf793e989c5975bcef0e712a550399c4ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325032"
---
# <a name="imedialocator-interface"></a>Interfaccia IMediaLocator

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IMediaLocator` interfaccia fornisce metodi per la convalida dei nomi di file in [DirectShow editing Services](directshow-editing-services.md) (des). Usare questa interfaccia per assicurarsi che un nome file e un percorso specificati corrispondano a un file esistente. Questa interfaccia fornisce inoltre un modo per cercare il file in altre posizioni e per visualizzare una finestra di dialogo **aperta** in modo che l'utente possa individuare il file.

Il localizzatore multimediale implementa questa interfaccia. La sequenza temporale e il motore di rendering supportano anche la convalida dei nomi di file tramite i metodi seguenti:

-   [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md): convalida e aggiorna i nomi di file nella sequenza temporale.
-   [**IRenderEngine:: SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md): specifica il modo in cui il motore di rendering convalida i nomi di file in fase di rendering.

In genere, un'applicazione DES chiamerà questi metodi anziché creare direttamente un'istanza del localizzatore multimediale. Per ulteriori informazioni, vedere [utilizzo del localizzatore multimediale](using-the-media-locator.md).

## <a name="members"></a>Membri

L'interfaccia **IMediaLocator** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMediaLocator** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IMediaLocator** dispone di questi metodi.



| Metodo                                                     | Descrizione                                                                        |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**AddFoundLocation**](imedialocator-addfoundlocation.md) | Aggiunge una directory alla cache di directory.<br/>                                |
| [**FindMediaFile**](imedialocator-findmediafile.md)       | Cerca un file e, in caso di esito positivo, recupera il percorso del file.<br/> |



 

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



 

 
