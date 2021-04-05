---
title: Proprietà DefaultCommand
description: Proprietà DefaultCommand
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d57d937cec575f0fdd99cc1f14511b9c88f9235
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046669"
---
# <a name="defaultcommand-property"></a>Proprietà DefaultCommand

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il comando predefinito dell'oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*Agent. * * * caratteri* *  **("***CharacterID***"). Stringa Commands. DefaultCommand** \[  =  \]



| Parte     | Descrizione                                                                         |
|----------|-------------------------------------------------------------------------------------|
| *string* | Valore stringa che identifica il nome (ID) del [**comando**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa proprietà consente di impostare un [**comando**](/windows/desktop/lwef/the-command-object) nella raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) come comando predefinito, eseguendone il rendering in grassetto. Questa operazione non modifica effettivamente la gestione dei comandi o gli eventi di doppio clic.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

 

 