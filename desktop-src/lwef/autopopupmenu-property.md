---
title: Proprietà AutoPopupMenu
description: Proprietà AutoPopupMenu
ms.assetid: 499092cb-0990-4edb-915c-12e3011de142
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d4ebfc559c88c3750a338f30b5dee4aad66ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331532"
---
# <a name="autopopupmenu-property"></a>Proprietà AutoPopupMenu

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un valore che indica se facendo clic con il pulsante destro del mouse sul carattere o sull'icona della barra delle applicazioni viene visualizzato automaticamente il menu popup del carattere

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente. ***Caratteri * * * * ("*** CharacterID * * *"). AutoPopupMenu*( *  \[  =  *booleano* )\]



| Parte      | Descrizione                                                                                                                                                                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Espressione booleana che specifica se il server Visualizza automaticamente il menu di scelta rapida del carattere facendo clic con il pulsante destro del mouse. **True** (impostazione predefinita) consente di visualizzare il menu facendo clic con il pulsante destro del mouse. <br/> **False** Il menu non viene visualizzato facendo clic con il pulsante destro del mouse.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Impostando questa proprietà su **false**, è possibile creare un comportamento personalizzato per la gestione dei menu. Per visualizzare il menu dopo l'impostazione di questa proprietà su **false**, utilizzare il metodo [**ShowPopupMenu**](showpopupmenu-method.md) .

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**Metodo ShowPopupMenu**](showpopupmenu-method.md)


 

 





