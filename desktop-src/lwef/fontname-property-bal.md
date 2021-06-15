---
title: Proprietà FontName (oggetto Balloon)
description: Informazioni sulla proprietà dell'oggetto Balloon FontName. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47e14935f913ce81b5faed5a49c3d731a73532f
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068267"
---
# <a name="fontname-property-balloon-object"></a>Proprietà FontName (oggetto Balloon)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il tipo di carattere utilizzato nel fumetto della parola per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Tipo di carattere Balloon.FontName_ *  \[  =  \]



| Parte   | Descrizione                                      |
|--------|--------------------------------------------------|
| *Carattere* | Valore stringa corrispondente al nome del tipo di carattere. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La [**proprietà FontName**](fontname-property.md) definisce il tipo di carattere usato per visualizzare il testo nella finestra del fumetto di una stringa. Il valore predefinito per le impostazioni del carattere del fumetto di un carattere viene impostato nell'editor di caratteri di Microsoft Agent. Inoltre, l'utente può eseguire l'override delle impostazioni dei caratteri per tutti i caratteri nella finestra delle proprietà di Microsoft Agent.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

> [!Note]  
> Se si usa un carattere che non è stato compilato, controllare le proprietà [**FontName**](fontname-property.md) e [**FontCharSet**](fontcharset-property.md) per il carattere per determinare se sono appropriate per le impostazioni locali. Potrebbe essere necessario impostare questi valori prima di usare il [**metodo Speak**](speak-method.md) per garantire la visualizzazione del testo appropriato all'interno del fumetto della parola.

 

 

 




