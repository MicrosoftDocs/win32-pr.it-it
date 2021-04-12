---
title: Proprietà della Guida
description: La proprietà Help fornisce informazioni che indicano all'utente la funzione di un oggetto.
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b240475d4583826e08fd6ee43b5839bdfb451d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329724"
---
# <a name="help-property"></a>Proprietà della Guida

La proprietà **Help** fornisce informazioni che indicano all'utente la funzione di un oggetto.

La proprietà della **Guida** viene recuperata chiamando [**IAccessible:: Get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).

Questa proprietà contiene informazioni di tipo Balloon (disponibili nelle descrizioni comandi) utilizzate per descrivere le operazioni svolte dall'oggetto o come utilizzarlo. Ad esempio, la proprietà **Help** per un pulsante della barra degli strumenti che mostra una stampante potrebbe fornire il testo seguente: "Prints the current document".

Non è necessario che il testo della proprietà della **Guida** sia univoco all'interno dell'interfaccia utente.

## <a name="when-to-support-the-help-property"></a>Quando supportare la proprietà della Guida

I server non supportano la proprietà della **Guida** se altre proprietà forniscono informazioni sufficienti sullo scopo dell'oggetto e sulle azioni eseguite dall'oggetto. Gli oggetti accessibili che espongono i controlli forniti dal sistema non supportano la proprietà della **Guida** .

 

 




