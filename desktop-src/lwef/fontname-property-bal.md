---
title: Proprietà FontName (oggetto Balloon)
description: Fontname (proprietà)
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead06323b36e86dce36163769b329140279f240d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118839"
---
# <a name="fontname-property-balloon-object"></a>Proprietà FontName (oggetto Balloon)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il tipo di carattere utilizzato nella parola Balloon per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*Agent. ***Characters ("**_CharacterID_*_")._ *  \[  =  *Tipo di carattere* Balloon. fontname\]



| Parte   | Descrizione                                      |
|--------|--------------------------------------------------|
| *carattere* | Valore stringa corrispondente al nome del tipo di carattere. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La proprietà [**fontname**](fontname-property.md) definisce il tipo di carattere utilizzato per visualizzare il testo nella finestra a fumetti di una stringa. Il valore predefinito per le impostazioni del tipo di carattere del fumetto di parole di un carattere viene impostato nell'editor dei caratteri di Microsoft Agent. Inoltre, l'utente può eseguire l'override delle impostazioni del tipo di carattere per tutti i caratteri nella finestra delle proprietà di Microsoft Agent.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

> [!Note]  
> Se si usa un carattere non compilato, controllare le proprietà [**fontname**](fontname-property.md) e [**FontCharSet**](fontcharset-property.md) per il carattere per determinare se sono appropriate per le impostazioni locali. Potrebbe essere necessario impostare questi valori prima di utilizzare il metodo [**Speak**](speak-method.md) per garantire la visualizzazione del testo appropriata all'interno del fumetto di Word.

 

 

 




