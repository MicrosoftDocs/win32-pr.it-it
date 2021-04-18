---
title: Proprietà HelpContextID (oggetto characters)
description: Proprietà HelpContextID
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42006f74cc3668f8df9af2c2ffcd2515614ec735
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400108"
---
# <a name="helpcontextid-property-characters-object"></a>Proprietà HelpContextID (oggetto characters)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un numero di contesto associato per il carattere. Utilizzato per fornire la Guida sensibile al contesto per il carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*Agent. ***Characters ("**_CharacterID_*_")._ *  \[  =  *Numero* HelpContextID\]



| Parte     | Descrizione                                   |
|----------|-----------------------------------------------|
| *Number* | Integer che specifica un numero di contesto valido. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Per supportare la Guida sensibile al contesto per il carattere, assegnare il numero di contesto al carattere usato per l'argomento della Guida associato quando si compila il file della guida. Questa proprietà si applica solo al client del carattere; l'impostazione non influisce sugli altri client del carattere o di altri caratteri del client.

Se è stato creato un file della Guida di Windows per l'applicazione e si è impostata [**la proprietà fileitem del carattere**](helpfile-property.md) , Agent chiama automaticamente la guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **true** e l'utente fa clic sul carattere. Se è presente un numero di contesto in [**HelpContextID**](helpcontextid-property.md), Agent chiama la guida e cerca l'argomento identificato dal numero di contesto corrente. Il numero di contesto corrente è il valore di **HelpContextID** per il carattere.

> [!Note]  
> La compilazione di un file della guida richiede il compilatore della Guida di Microsoft Windows.

 

## <a name="see-also"></a>Vedere anche

[**Proprietà filelima**](helpfile-property.md)


 

 




