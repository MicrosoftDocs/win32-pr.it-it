---
title: Hide (metodo)
description: Hide (metodo)
ms.assetid: c30eda78-0951-43b4-8ae1-daccbd41170d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd50c3f7b8e3d2e60ebe4c00c42375737c05eb04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117675"
---
# <a name="hide-method"></a>Hide (metodo)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Nasconde il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *"). Nascondi* *  \[ *veloce*\]



| Parte   | Descrizione                                                                                                                                                                                                                                      |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Veloce* | facoltativo. Valore booleano che indica se ignorare l'animazione associata allo stato nascosto del carattere **true** non riproduce l'animazione **nascosta** . <br/> **False** (impostazione predefinita) riproduce l'animazione **nascosta** . <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Il server accoda le azioni del metodo **Hide** nella coda del carattere, quindi è possibile usarlo per nascondere il carattere dopo una sequenza di altre animazioni. È possibile riprodurre l'azione immediatamente usando il metodo [**Stop**](stop-method.md) prima di chiamare questo metodo.

Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito un oggetto [**Request**](/windows/desktop/lwef/the-request-object) . Inoltre, se l'animazione **nascosta** associata non è stata caricata e non è stato specificato il parametro **Fast** su **true**, il server imposta la proprietà **Request** Object [**status**](status-property.md) su "failed" con un numero di errore appropriato. Se pertanto si utilizza il protocollo HTTP per accedere ai dati di tipo carattere o di animazione, **utilizzare il metodo** [**Get**](get-method.md) e specificare lo stato Hide per caricare l'animazione prima di chiamare il metodo **Hide** .

Il nascondere un carattere può anche causare l'attivazione dell'evento [**ActivateInput**](activateinput-event.md) di un altro client.

> [!Note]  
> I caratteri nascosti non possono accedere al canale audio. Il server restituirà uno stato di errore nell'evento [**RequestComplete**](requestcomplete-event.md) se si genera una richiesta di animazione e il carattere è nascosto.

 

## <a name="see-also"></a>Vedere anche

[**Show (metodo)**](show-method.md)


 

