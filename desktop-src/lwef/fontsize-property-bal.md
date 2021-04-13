---
title: Proprietà FontSize (oggetto Balloon)
description: Proprietà FontSize
ms.assetid: 36d5526a-1ae9-4ef2-94f6-0ad63ce86882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569c07e98fb8bf973a554e89655f71e816b4a51b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400156"
---
# <a name="fontsize-property-balloon-object"></a>Proprietà FontSize (oggetto Balloon)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta la dimensione del carattere supportata per la parola Balloon per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*Agent. * * * caratteri* *  **("**_CharacterID_*_"). Punti di Balloon. FontSize_* \[  =  \]



| Parte     | Descrizione                                              |
|----------|----------------------------------------------------------|
| *Punti* | Valore long integer che specifica la dimensione del carattere in punti. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La proprietà [**FontSize**](fontsize-property.md) restituisce un valore long integer che specifica la dimensione corrente del carattere in punti. Il valore massimo per **FontSize** è 2160 punti.

Il valore predefinito per le impostazioni del tipo di carattere del fumetto di parole di un carattere viene impostato nell'editor dei caratteri di Microsoft Agent. Inoltre, l'utente può eseguire l'override delle impostazioni del tipo di carattere per tutti i caratteri nella finestra delle proprietà di Microsoft Agent.

 

 




