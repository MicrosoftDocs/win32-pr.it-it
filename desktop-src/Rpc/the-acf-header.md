---
title: Intestazione ACF
description: L'intestazione ACF contiene attributi specifici della piattaforma che si applicano all'interfaccia nel suo complesso. Gli attributi applicati a singoli tipi e funzioni nel corpo di ACF eseguono l'override degli attributi nell'intestazione ACF. Nessun attributo obbligatorio nell'intestazione ACF.
ms.assetid: c09ec0f2-2302-450a-b74b-c9008beca325
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e958044f043db8828f0fdda192918c632c321b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047023"
---
# <a name="the-acf-header"></a>Intestazione ACF

L'intestazione ACF contiene attributi specifici della piattaforma che si applicano all'interfaccia nel suo complesso. Gli attributi applicati a singoli tipi e funzioni nel corpo di ACF eseguono l'override degli attributi nell'intestazione ACF. Nessun attributo obbligatorio nell'intestazione ACF.

L'intestazione ACF può includere uno degli attributi seguenti: **\[** [**\_ handle automatico**](/windows/desktop/Midl/auto-handle) **\]** , **\[** [**\_ handle implicito**](/windows/desktop/Midl/implicit-handle) **\]** o [**\_ handle esplicito**](/windows/desktop/Midl/explicit-handle) **\]** . Se viene utilizzato l'handle **\[ automatico \_ \]** o l' **\[ \_ handle \] implicito** , viene specificato il tipo di handle di associazione che verrà utilizzato per l'associazione quando una funzione remota non dispone di un parametro di handle di binding esplicito. Quando ACF non è presente o non specifica un handle di binding automatico, implicito o esplicito, MIDL usa l' **\[ \_ handle \] automatico** per l'associazione implicita.

Il **\[** [**codice**](/windows/desktop/Midl/code) **\]** o **\[** [**NoCode**](/windows/desktop/Midl/nocode) **\]** può essere visualizzato nell'intestazione dell'interfaccia, ma quello scelto può apparire una sola volta. Quando nessuno degli attributi è presente, il compilatore usa il **\[ codice \]** come valore predefinito.

Per altre informazioni, vedere [attributi ACF](/windows/desktop/Midl/acf-attributes).

 

 