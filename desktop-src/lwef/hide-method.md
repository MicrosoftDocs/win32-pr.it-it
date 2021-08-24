---
title: Metodo Hide
description: Metodo Hide
ms.assetid: c30eda78-0951-43b4-8ae1-daccbd41170d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67057464c8e505e56123f712d3a1e6d668c7d75b00bc4732e7b18195b3be9723
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725451"
---
# <a name="hide-method"></a>Metodo Hide

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Nasconde il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Nascondi_ *  \[ *veloce*\]



| Parte   | Descrizione                                                                                                                                                                                                                                      |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Veloce* | facoltativo. Valore booleano che indica se ignorare l'animazione associata allo stato Nascondi **true** del carattere Non riproduce **l'animazione Nascondi.** <br/> **False** (impostazione predefinita) Riproduce **l'animazione Nascondi.** <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Il server accoda le azioni del metodo **Hide** nella coda del carattere, quindi è possibile usarlo per nascondere il carattere dopo una sequenza di altre animazioni. È possibile riprodurre l'azione immediatamente usando il [**metodo Stop**](stop-method.md) prima di chiamare questo metodo.

Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito [**un oggetto Request.**](/windows/desktop/lwef/the-request-object) Inoltre, se l'animazione **Nascondi** associata non è stata caricata e non è stato specificato il parametro **Fast** come **True,** il server imposta la proprietà **Request** object [**Status**](status-property.md) su "failed" con un numero di errore appropriato. Pertanto, se si usa il protocollo HTTP per accedere ai dati di carattere o animazione, usare il [**metodo Get**](get-method.md) e specificare lo **stato Nascondi** per caricare l'animazione prima di chiamare il **metodo Hide.**

Nascondere un carattere può anche causare l'attivazione [**dell'evento ActivateInput**](activateinput-event.md) di un altro client.

> [!Note]  
> I caratteri nascosti non possono accedere al canale audio. Il server passerà nuovamente uno stato di errore nell'evento [**RequestComplete**](requestcomplete-event.md) se si genera una richiesta di animazione e il carattere è nascosto.

 

## <a name="see-also"></a>Vedere anche

[**Show (metodo)**](show-method.md)


 

