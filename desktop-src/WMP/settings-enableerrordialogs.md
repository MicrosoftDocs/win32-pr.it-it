---
title: Impostazioni.enableErrorDialogs
description: La proprietà enableErrorDialogs specifica o recupera un valore che indica se le finestre di dialogo di errore vengono visualizzate automaticamente.
ms.assetid: 16b10bea-4b3e-469f-a903-02f19ffcdf31
keywords:
- Impostazioni.enableErrorDialogs Windows Media Player
topic_type:
- apiref
api_name:
- Settings.enableErrorDialogs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa786606a97edcfca22512dd0b3188a06a7851f8bab2401e139d7ead2c3495ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569373"
---
# <a name="settingsenableerrordialogs"></a>Impostazioni.enableErrorDialogs

La **proprietà enableErrorDialogs** specifica o recupera un valore che indica se le finestre di dialogo di errore vengono visualizzate automaticamente.

## <a name="syntax"></a>Sintassi

player.settings.enableErrorDialogs

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un valore booleano di **lettura/scrittura.**



| Valore | Descrizione                                     |
|-------|-------------------------------------------------|
| true  | Valore predefinito. Le finestre di dialogo di errore vengono visualizzate automaticamente. |
| false | Le finestre di dialogo di errore non vengono visualizzate automaticamente.      |



 

## <a name="remarks"></a>Commenti

Questa proprietà presenta un comportamento specifico per le istanze remote del controllo Player. Per altre informazioni, vedere [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostazioni Oggetto**](settings-object.md)
</dt> </dl>

 

 





