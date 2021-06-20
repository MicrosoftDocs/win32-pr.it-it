---
description: Implementare una pagina delle proprietà come parte della creazione di una pagina delle proprietà di filtro per un filtro DirectShow personalizzato.
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: Passaggio 4. Creare la pagina delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32cd9eacc98af5f273897a3837390ab5cc75f7a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406854"
---
# <a name="step-4-create-the-property-page"></a>Passaggio 4. Creare la pagina delle proprietà

A questo punto il filtro supporta tutti gli elementi di cui ha bisogno per una pagina delle proprietà. Il passaggio successivo consiste nell'implementazione della pagina delle proprietà stessa. Per iniziare, derivare una nuova classe da **CBasePropertyPage**. L'esempio seguente illustra parte della dichiarazione, incluse alcune variabili membro private che verranno usate più avanti nell'esempio:


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



Creare quindi una risorsa finestra di dialogo nell'editor di risorse, insieme a una risorsa stringa per il titolo della finestra di dialogo. La stringa verrà visualizzata nella scheda della pagina delle proprietà. I due ID risorsa sono argomenti per il **costruttore CBasePropertyPage:**


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



La figura seguente mostra la risorsa finestra di dialogo per la pagina delle proprietà di esempio.

![finestra di dialogo della pagina delle proprietà](images/proppage.png)

A questo punto è possibile implementare la pagina delle proprietà. Di seguito sono descritti i metodi in **CBasePropertyPage di** cui eseguire l'override:

-   **OnConnect** viene chiamato quando il client crea la pagina delle proprietà. Imposta il **puntatore IUnknown** sul filtro.
-   **OnActivate** viene chiamato quando viene creata la finestra di dialogo.
-   **OnReceiveMessage viene** chiamato quando la finestra di dialogo riceve un messaggio di finestra.
-   **OnApplyChanges viene** chiamato quando l'utente esegue il commit delle modifiche alle proprietà facendo clic sul **pulsante OK** **o** Applica.
-   **OnDisconnect viene** chiamato quando l'utente chiude la finestra delle proprietà.

La parte restante di questa esercitazione descrive ognuno di questi metodi.

Successivo: [Passaggio 5. Archiviare un puntatore al filtro](step-5--store-a-pointer-to-the-filter.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una pagina delle proprietà Filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



