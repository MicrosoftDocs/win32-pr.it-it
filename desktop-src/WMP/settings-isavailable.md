---
title: Impostazioni.isAvailable
description: La proprietà isAvailable indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata. | Impostazioni.isAvailable
ms.assetid: 89403125-545c-482b-a27e-6fee06abe247
keywords:
- Impostazioni.isAvailable Windows Media Player
topic_type:
- apiref
api_name:
- Settings.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df10026007dd9e04fe88d634a3da566074b0d6a88420ef444d5f2bae39a793fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002411"
---
# <a name="settingsisavailable"></a>Impostazioni.isAvailable

La **proprietà isAvailable** indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.

## <a name="syntax"></a>Sintassi

player.settings.isAvailable( name )

## <a name="parameters"></a>Parametri

*nome*

Stringa contenente uno dei valori seguenti.



| string             | Descrizione                                                    |
|--------------------|----------------------------------------------------------------|
| avvio automatico          | Determina se è possibile impostare la proprietà autoStart.          |
| Balance            | Determina se è possibile impostare la proprietà balance.            |
| BaseURL            | Determina se è possibile impostare la proprietà baseURL.            |
| DefaultFrame       | Determina se è possibile impostare la proprietà defaultFrame.       |
| EnableErrorDialogs | Determina se è possibile impostare la proprietà enableErrorDialogs. |
| GetMode            | Determina se è possibile chiamare il metodo getMode.           |
| InvokeURLs         | Determina se è possibile impostare la proprietà invokeURLs.         |
| Disattiva audio               | Determina se è possibile impostare la proprietà mute.               |
| PlayCount          | Determina se è possibile impostare la proprietà playCount.          |
| Tariffa               | Determina se la proprietà rate può essere impostata.               |
| SetMode            | Determina se è possibile chiamare il metodo setMode.           |
| Volume             | Determina se è possibile impostare la proprietà del volume.             |



 

## <a name="return-values"></a>Valori restituiti

Questo metodo restituisce un **valore booleano.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostazioni Oggetto**](settings-object.md)
</dt> </dl>

 

 





