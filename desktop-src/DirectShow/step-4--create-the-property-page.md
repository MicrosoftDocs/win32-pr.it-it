---
description: Passaggio 4.
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: Passaggio 4. Creazione della pagina delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e8ea1a22e30c57c66b263a62afc1e0cf801903
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234367"
---
# <a name="step-4-create-the-property-page"></a>Passaggio 4. Creazione della pagina delle proprietà

A questo punto il filtro supporta tutti gli elementi necessari per una pagina delle proprietà. Il passaggio successivo consiste nell'implementazione della pagina delle proprietà. Per iniziare, derivare una nuova classe da **CBasePropertyPage**. Nell'esempio seguente viene illustrata una parte della dichiarazione, incluse alcune variabili membro private che verranno utilizzate più avanti nell'esempio:


```C++
class CGrayProp : public CBasePropertyPage
{
private:
    ISaturation *m_pGray;    // Pointer to the filter's custom interface.
    long        m_lVal       // Store the old value, so we can revert.
    long        m_lNewVal;   // New value.
public:
    /* ... */
};
```



Successivamente, creare una risorsa finestra di dialogo nell'editor di risorse, insieme a una risorsa di stringa per il titolo della finestra di dialogo. La stringa verrà visualizzata nella scheda della pagina delle proprietà. I due ID risorsa sono argomenti del costruttore **CBasePropertyPage** :


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



Nella figura seguente viene illustrata la risorsa finestra di dialogo per la pagina delle proprietà di esempio.

![finestra di dialogo della pagina delle proprietà](images/proppage.png)

A questo punto è possibile implementare la pagina delle proprietà. Ecco i metodi in **CBasePropertyPage** per eseguire l'override:

-   **OnConnect** viene chiamato quando il client crea la pagina delle proprietà. Imposta il puntatore **IUnknown** sul filtro.
-   **OnActivate** viene chiamato quando viene creata la finestra di dialogo.
-   **OnReceiveMessage** viene chiamato quando la finestra di dialogo riceve un messaggio di finestra.
-   **OnApplyChanges** viene chiamato quando l'utente esegue il commit delle modifiche delle proprietà facendo clic sul pulsante **OK** o **applica** .
-   **Disconnect** viene chiamato quando l'utente dimentica la finestra delle proprietà.

Nella parte restante di questa esercitazione vengono descritti ognuno di questi metodi.

Successivo: [passaggio 5. Consente di archiviare un puntatore al filtro](step-5--store-a-pointer-to-the-filter.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una pagina delle proprietà del filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



