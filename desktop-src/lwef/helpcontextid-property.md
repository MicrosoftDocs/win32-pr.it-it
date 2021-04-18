---
title: Proprietà HelpContextID (oggetto Collection Commands)
description: Proprietà HelpContextID
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d530a1563080108ef2a2798589519ecca03416
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474921"
---
# <a name="helpcontextid-property-commands-collection-object"></a>Proprietà HelpContextID (oggetto Collection Commands)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un numero di contesto associato per l'oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . Utilizzato per fornire la Guida sensibile al contesto per l'oggetto **Commands** .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*Agent. ***Characters ("**_CharacterID_*_"). Comandi ("_*_Name_*_")._ *  \[  =  *Numero* HelpContextID\]



| Parte     | Descrizione                                   |
|----------|-----------------------------------------------|
| *Number* | Integer che specifica un numero di contesto valido. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se è stato creato un file della Guida di Windows per l'applicazione e si è impostata la proprietà filecommand [**del carattere**](helpfile-property.md) , Agent chiama automaticamente la guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **true** e l'utente seleziona l'oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . Se si imposta un numero di contesto in **HelpContextID**, Agent chiama la guida e cerca l'argomento identificato da tale numero di contesto.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

> [!Note]  
> La compilazione di un file della guida richiede il compilatore della Guida di Microsoft Windows.

 

## <a name="see-also"></a>Vedere anche

[**Proprietà filelima**](helpfile-property.md)


 

 
