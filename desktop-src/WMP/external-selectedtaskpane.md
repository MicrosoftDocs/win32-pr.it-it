---
title: External.SelectedTaskPane
description: Nota Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di un negozio online non è supportato. La proprietà SelectedTaskPane specifica o recupera il riquadro attività attualmente selezionato.
ms.assetid: af7b4627-1336-444c-9b4e-5f2e07d9eea7
keywords:
- External.SelectedTaskPane Windows Media Player
topic_type:
- apiref
api_name:
- External.SelectedTaskPane
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e49225be7bbdb5ce128a793d3c88409ef9d994ef5017c57b5f12738b62eaa5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736191"
---
# <a name="externalselectedtaskpane"></a>External.SelectedTaskPane

> [!Note]  
> In questo argomento vengono descritte le funzionalità progettate per l'utilizzo da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di un negozio online non è supportato.

 

La **proprietà SelectedTaskPane** specifica o recupera il riquadro attività attualmente selezionato.

## <a name="syntax"></a>Sintassi

window.external.SelectedTaskPane = *servicetask*

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di **lettura/scrittura.** I valori possibili sono "ServiceTask1", "ServiceTask2" e "ServiceTask3".

## <a name="remarks"></a>Commenti

Se si specifica un valore per questa proprietà, viene evidenziato il pulsante per tale riquadro. Non rende attivo il riquadro attività specificato. È necessario specificare un valore per questa proprietà per impostare il pulsante del riquadro attività corrente per la pagina Web quando la pagina viene caricata per assicurarsi che sia attivo il pulsante del riquadro attività corretto.

Per rendere attivo un determinato riquadro attività, usare il **metodo NavigateTaskPaneURL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per negozi online di tipo 2**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**External.NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> </dl>

 

 





