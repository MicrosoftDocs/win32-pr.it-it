---
title: Proprietà DefaultCommand
description: Proprietà DefaultCommand
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7aec703ffbabb98ae16609b0dcb01767fda5c38b42ed40f204e3a3bae5766
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693636"
---
# <a name="defaultcommand-property"></a>Proprietà DefaultCommand

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il comando predefinito [**dell'oggetto Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Caratteri* *  **("**_CharacterID_*_"). Stringa Commands.DefaultCommand_* \[  =  \]



| Parte     | Descrizione                                                                         |
|----------|-------------------------------------------------------------------------------------|
| *string* | Valore stringa che identifica il nome (ID) del [**comando**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa proprietà consente di impostare un [**oggetto Command**](/windows/desktop/lwef/the-command-object) nella raccolta [**Commands**](/windows/desktop/lwef/the-commands-collection-object) come comando predefinito, rendendolo in grassetto. Ciò non modifica effettivamente la gestione dei comandi o gli eventi di doppio clic.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. L'impostazione non influisce su altri client del carattere o di altri caratteri dell'applicazione client.

 

 