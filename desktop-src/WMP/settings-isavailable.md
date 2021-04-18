---
title: Settings. available
description: La proprietà disavailable indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata. | Settings. available
ms.assetid: 89403125-545c-482b-a27e-6fee06abe247
keywords:
- Impostazioni. Media Player Windows disponibile
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
ms.openlocfilehash: a96923fa57ffab4fb2e47b16afd03a06bbffd0ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327382"
---
# <a name="settingsisavailable"></a>Settings. available

La proprietà **disavailable** indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.

## <a name="syntax"></a>Sintassi

Player. Settings. available (nome)

## <a name="parameters"></a>Parametri

*nome*

Stringa contenente uno dei valori seguenti.



| string             | Descrizione                                                    |
|--------------------|----------------------------------------------------------------|
| avvio automatico          | Determina se è possibile impostare la proprietà di avvio automatico.          |
| Balance            | Determina se è possibile impostare la proprietà Balance.            |
| BaseURL            | Determina se è possibile impostare la proprietà baseURL.            |
| DefaultFrame       | Determina se è possibile impostare la proprietà defaultFrame.       |
| EnableErrorDialogs | Determina se è possibile impostare la proprietà enableErrorDialogs. |
| GetMode            | Determina se è possibile chiamare il metodo GetMode.           |
| InvokeURLs         | Determina se è possibile impostare la proprietà invokeURLs.         |
| Disattiva audio               | Determina se è possibile impostare la proprietà mute.               |
| PlayCount          | Determina se è possibile impostare la proprietà playCount.          |
| Tariffa               | Determina se è possibile impostare la proprietà rate.               |
| SetMode            | Determina se è possibile chiamare il metodo semode.           |
| Volume             | Determina se è possibile impostare la proprietà del volume.             |



 

## <a name="return-values"></a>Valori restituiti

Questo metodo restituisce un valore **booleano** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Settings**](settings-object.md)
</dt> </dl>

 

 





