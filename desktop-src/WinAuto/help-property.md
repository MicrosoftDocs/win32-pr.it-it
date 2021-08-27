---
title: Proprietà Help
description: La proprietà Help fornisce informazioni che comunicano all'utente la funzione di un oggetto.
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6f8b226c483e3a3d68f878fccb940fc1a9f69f18b6fde62eed4b5a7a8ea9b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122191"
---
# <a name="help-property"></a>Proprietà Help

La **proprietà Help** fornisce informazioni che comunicano all'utente la funzione di un oggetto.

La **proprietà Help** viene recuperata chiamando [**IAccessible::get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).

Questa proprietà contiene informazioni di tipo fumetto (come si trova nelle descrizioni comandi) usate per descrivere il funzionamento dell'oggetto o come usarlo. Ad esempio, la **proprietà Guida** per un pulsante della barra degli strumenti che mostra una stampante potrebbe fornire il testo seguente: "Stampa il documento corrente".

Il testo per la **proprietà Help** non deve essere univoco all'interno dell'interfaccia utente.

## <a name="when-to-support-the-help-property"></a>Quando supportare la proprietà Help

I server non supportano la **proprietà Della** Guida se altre proprietà forniscono informazioni sufficienti sullo scopo dell'oggetto e sulle azioni eseguite dall'oggetto. Gli oggetti accessibili che espongono controlli forniti dal sistema non supportano la **proprietà Della** Guida.

 

 




