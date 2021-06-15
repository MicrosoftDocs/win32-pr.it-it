---
title: Proprietà HelpContextID (oggetto Characters)
description: Informazioni sulla proprietà HelpContextID dell'oggetto Characters. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e751cb2d8834a6af2c3b816066d6051e3a28c767
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068187"
---
# <a name="helpcontextid-property-characters-object"></a>Proprietà HelpContextID (oggetto Characters)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un numero di contesto associato per il carattere. Utilizzato per fornire la Guida sensibile al contesto per il carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). HelpContextID_ *  \[  =  *Number*\]



| Parte     | Descrizione                                   |
|----------|-----------------------------------------------|
| *Number* | Intero che specifica un numero di contesto valido. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Per supportare la Guida sensibile al contesto per il carattere, assegnare il numero di contesto al carattere utilizzato per l'argomento della Guida associato quando si compila il file della Guida. Questa proprietà si applica solo al client del carattere. L'impostazione non influisce sugli altri client del carattere o di altri caratteri del client.

Se è stato creato un file della Guida di Windows per l'applicazione e si è impostata la proprietà [**HelpFile**](helpfile-property.md) del carattere, Agent chiama automaticamente help quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **True** e l'utente fa clic sul carattere. Se è presente un numero di contesto in [**HelpContextID**](helpcontextid-property.md), Agent chiama la Guida e cerca l'argomento identificato dal numero di contesto corrente. Il numero di contesto corrente è il valore **di HelpContextID** per il carattere.

> [!Note]  
> La compilazione di un file della Guida richiede il compilatore della Guida di Microsoft Windows.

 

## <a name="see-also"></a>Vedere anche

[**Proprietà HelpFile**](helpfile-property.md)


 

 




