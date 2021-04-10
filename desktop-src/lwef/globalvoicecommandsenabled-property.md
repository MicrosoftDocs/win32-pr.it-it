---
title: Proprietà GlobalVoiceCommandsEnabled
description: Proprietà GlobalVoiceCommandsEnabled
ms.assetid: d4f74019-fa33-41fc-abe7-01791ff188f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f523171187c9956a7741afc0fabcc7ec794071
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963093"
---
# <a name="globalvoicecommandsenabled-property"></a>Proprietà GlobalVoiceCommandsEnabled

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un valore che indica se la voce è abilitata per i comandi globali dell'agente.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente. ***Caratteri ("*** CharacterID * * *"). Commands. GlobalVoiceCommandsEnabled**

\[ = *Boolean*\]



| Parte      | Descrizione                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Espressione booleana che indica se i parametri vocali per i comandi globali dell'agente sono abilitati. **True** (impostazione predefinita) i parametri vocali sono abilitati. <br/> **False** I parametri vocali sono disabilitati.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Microsoft Agent aggiunge automaticamente i parametri vocali (grammatica) per l'apertura e la chiusura della finestra dei comandi vocali e per visualizzare e nascondere il carattere. Se si imposta **GlobalVoiceCommandsEnabled** su **false**, Agent Disabilita tutti i parametri vocali per questi comandi, nonché i parametri vocali per la [**didascalia**](caption-property.md) degli oggetti [**comandi**](/windows/desktop/lwef/the-commands-collection-object) di altri client. In questo modo è possibile eliminarli dalla grammatica attiva corrente del client. Tuttavia, poiché questo potrebbe bloccare l'accesso vocale ad altri client, reimpostare questa proprietà su **true** dopo l'elaborazione dell'input vocale dell'utente.

La disabilitazione della proprietà non influisce sul menu di scelta rapida del carattere. Verranno comunque visualizzati i comandi globali aggiunti dal server. Non è possibile rimuoverli dal menu a comparsa.

 

