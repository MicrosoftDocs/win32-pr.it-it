---
title: AccNameContainsInvalidString
description: AccNameContainsInvalidString
ms.assetid: 392E4D10-4A8E-4118-B0E7-F74571812043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670672769c22cba556c164b8d03b2e9148fb8b1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298881"
---
# <a name="accnamecontainsinvalidstring"></a>AccNameContainsInvalidString

## <a name="text"></a>Testo

accName non deve contenere la stringa {0}

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Il nome di un elemento contiene caratteri non validi. questi caratteri sono sostituiti da AccChecker. Ad esempio, il metodo [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) usato per recuperare il nome MSAA di un elemento restituisce una stringa che contiene i caratteri di tabulazione, nuova riga o e commerciale.

Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché un elemento potrebbe avere un nome non pronunciabile e non intuitivo.

## <a name="possible-causes"></a>Possibili cause

All'elemento o al relativo padre è assegnato un nome o un'etichetta non corretta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible:: Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Proprietà Name](name-property.md)
</dt> </dl>

 

 




