---
title: AccNameLengthTooLong
description: AccNameLengthTooLong
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1efcb2b7d13c83a5972cb6e100d70500f9c5ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298880"
---
# <a name="accnamelengthtoolong"></a>AccNameLengthTooLong

## <a name="text"></a>Testo

Il nome dell'elemento non deve restituire una stringa più lunga di un {0} carattere

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Il nome di un elemento contiene troppi caratteri. Ad esempio, il metodo [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) usato per recuperare il nome MSAA di un elemento restituisce una stringa superiore al limite di 32000 caratteri.

Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché un elemento potrebbe avere un nome non pronunciabile e non intuitivo.

## <a name="possible-causes"></a>Possibili cause

All'elemento o al relativo padre è assegnato un nome o un'etichetta non corretta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible:: Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Proprietà Name](name-property.md)
</dt> </dl>

 

 




