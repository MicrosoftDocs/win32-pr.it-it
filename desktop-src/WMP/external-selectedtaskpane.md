---
title: External. SelectedTaskPane
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. La proprietà SelectedTaskPane specifica o Recupera il riquadro attività attualmente selezionato.
ms.assetid: af7b4627-1336-444c-9b4e-5f2e07d9eea7
keywords:
- Media Player di Windows External. SelectedTaskPane
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
ms.openlocfilehash: 28535e0497362a2153bcaad439425174e9c1bdc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324542"
---
# <a name="externalselectedtaskpane"></a>External. SelectedTaskPane

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

La proprietà **SelectedTaskPane** specifica o Recupera il riquadro attività attualmente selezionato.

## <a name="syntax"></a>Sintassi

Window. External. SelectedTaskPane = *servicetask*

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di lettura/scrittura. I valori possibili sono "ServiceTask1", "ServiceTask2" e "ServiceTask3".

## <a name="remarks"></a>Commenti

Se si specifica un valore per questa proprietà, viene evidenziato il pulsante relativo a tale riquadro. Non rende attivo il riquadro attività specificato. È necessario specificare un valore per questa proprietà per impostare il pulsante del riquadro attività corrente per la pagina Web quando viene caricata la pagina per assicurarsi che il pulsante riquadro attività corretto sia attivo.

Per rendere attivo uno specifico riquadro attività, utilizzare il metodo **NavigateTaskPaneURL** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 2 online**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**External. NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> </dl>

 

 





