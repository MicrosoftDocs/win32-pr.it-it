---
title: AccNameLengthTooLong
description: AccNameLengthTooLong
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9df4b9001460b9ad96cf5c987a0e8c744ec8df183901494311275052ea4146
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327707"
---
# <a name="accnamelengthtoolong"></a>AccNameLengthTooLong

## <a name="text"></a>Testo

Il nome dell'elemento non deve restituire una stringa più lunga del {0} carattere

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Il nome di un elemento contiene troppi caratteri. Ad esempio, il [**metodo get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) usato per recuperare il nome MSAA di un elemento restituisce una stringa maggiore del limite di 32000 caratteri.

Questo problema causa problemi per gli utenti che si affidano a un'utilità per la lettura dello schermo e a una tastiera per lo spostamento, perché un elemento potrebbe avere un nome non intuitivo e imprevedibile.

## <a name="possible-causes"></a>Possibili cause

All'elemento o al relativo elemento padre è assegnato un nome o un'etichetta non corretta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Proprietà Name](name-property.md)
</dt> </dl>

 

 




