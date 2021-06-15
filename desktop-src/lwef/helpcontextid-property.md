---
title: Proprietà HelpContextID (oggetto raccolta Commands)
description: Informazioni sulla proprietà HelpContextID dell'oggetto raccolta Commands. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ed6ccf40545e15b3603ce5abe80ef94ff4272a
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068237"
---
# <a name="helpcontextid-property-commands-collection-object"></a>Proprietà HelpContextID (oggetto raccolta Commands)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un numero di contesto associato per [**l'oggetto**](/windows/desktop/lwef/the-commands-collection-object) Commands. Usato per fornire la Guida sensibile al contesto per **l'oggetto** Commands.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands("_*_name_*_"). HelpContextID_ *  \[  =  *Number*\]



| Parte     | Descrizione                                   |
|----------|-----------------------------------------------|
| *Number* | Intero che specifica un numero di contesto valido. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se è stato creato un file della Guida di Windows per l'applicazione e si è impostata la proprietà [**HelpFile**](helpfile-property.md) del carattere, Agent chiama automaticamente help quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **True** e l'utente seleziona l'oggetto [**Commands.**](/windows/desktop/lwef/the-commands-collection-object) Se si imposta un numero di contesto in **HelpContextID**, Agent chiama la Guida e cerca l'argomento identificato da tale numero di contesto.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. L'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

> [!Note]  
> La compilazione di un file della Guida richiede il compilatore della Guida di Microsoft Windows.

 

## <a name="see-also"></a>Vedere anche

[**Proprietà HelpFile**](helpfile-property.md)


 

 
