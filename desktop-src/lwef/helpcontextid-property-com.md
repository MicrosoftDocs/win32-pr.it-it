---
title: Proprietà HelpContextID (oggetto Command)
description: Informazioni sulla proprietà HelpContextID dell'oggetto Command. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461c3c0ff5a6722dd6740c7df7e89bf2b9520053
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068513"
---
# <a name="helpcontextid-property-command-object"></a>Proprietà HelpContextID (oggetto Command)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un numero di contesto associato per [**l'oggetto**](/windows/desktop/lwef/the-command-object) Command. Usato per fornire la Guida sensibile al contesto per **l'oggetto** Command.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands(""). Numero_ *  \[  =  *HelpContextID*\]



| Parte     | Descrizione                                   |
|----------|-----------------------------------------------|
| *Number* | Intero che specifica un numero di contesto valido. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se è stato creato un file della Guida di Windows per l'applicazione e si imposta la proprietà [**HelpFile**](helpfile-property.md) del carattere sul file, Agent chiama automaticamente la Guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **True** e l'utente seleziona il comando. Se si imposta un numero di contesto in [**HelpContextID,**](helpcontextid-property.md)Agent chiama la Guida e cerca l'argomento identificato dal numero di contesto corrente. Il numero di contesto corrente è il valore **di HelpContextID** per il comando.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

> [!Note]  
> La compilazione di un file della Guida richiede il compilatore della Guida di Microsoft Windows.

 

## <a name="see-also"></a>Vedere anche

[**Proprietà HelpFile**](helpfile-property.md)


 

 
