---
title: Proprietà GlobalVoiceCommandsEnabled
description: Proprietà GlobalVoiceCommandsEnabled
ms.assetid: d4f74019-fa33-41fc-abe7-01791ff188f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f889d242afca406ba443fd3d9a19afb837fbed0390f5c0c3d2bbd2ac2ccbccb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751445"
---
# <a name="globalvoicecommandsenabled-property"></a>Proprietà GlobalVoiceCommandsEnabled

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un valore che indica se la voce è abilitata per i comandi globali di Agent.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands.GlobalVoiceCommandsEnabled_*

\[ = *Boolean*\]



| Parte      | Descrizione                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Espressione booleana che indica se i parametri vocali per i comandi globali di Agent sono abilitati. **True** (impostazione predefinita) I parametri vocali sono abilitati. <br/> **False** I parametri vocali sono disabilitati.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Microsoft Agent aggiunge automaticamente i parametri vocali (grammatica) per l'apertura e la chiusura della finestra Comandi vocali e per visualizzare e nascondere il carattere. Se si imposta **GlobalVoiceCommandsEnabled** su **False,** Agent disabilita tutti i parametri vocali [](caption-property.md) per questi comandi, nonché i parametri vocali per la didascalia degli oggetti [**Commands**](/windows/desktop/lwef/the-commands-collection-object) di altri client. In questo modo è possibile eliminarli dalla grammatica attiva corrente del client. Tuttavia, poiché potenzialmente blocca l'accesso vocale ad altri client, reimpostare questa proprietà su **True** dopo l'elaborazione dell'input vocale dell'utente.

La disabilitazione della proprietà non influisce sul menu a comparsa del carattere. Verranno comunque visualizzati i comandi globali aggiunti dal server. Non è possibile rimuoverli dal menu a comparsa.

 

