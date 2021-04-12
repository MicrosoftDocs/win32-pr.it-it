---
title: Cursor (riferimento all'elemento dell'interfaccia utente MSAA)
description: Un cursore è una piccola immagine il cui percorso sullo schermo è controllato da un dispositivo di puntamento, ad esempio un mouse, una penna o una trackball. Quando l'utente sposta il dispositivo di puntamento, il sistema operativo Windows sposta il cursore.
ms.assetid: ff97d474-7c96-4f89-bc34-2cf320381ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff351040d342adccda8cb03d56d91f9dc429074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328852"
---
# <a name="cursor-msaa-ui-element-reference"></a>Cursor (riferimento all'elemento dell'interfaccia utente MSAA)

> [!Note]  
> In questo argomento vengono descritti i cursori ai fini del riferimento all'elemento dell'interfaccia utente MSAA. L'uso di cursori in diversi framework dell'interfaccia utente non è descritto qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

Un cursore è una piccola immagine il cui percorso sullo schermo è controllato da un dispositivo di puntamento, ad esempio un mouse, una penna o una trackball. Quando l'utente sposta il dispositivo di puntamento, il sistema operativo Windows sposta il cursore.

## <a name="iaccessible-methods"></a>Metodi IAccessible

Un cursore supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Un cursore supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount): la proprietà **childCount** è zero.
-   [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): gli sviluppatori possono creare cursori personalizzati o usare i cursori predefiniti identificati dall'ID del cursore. La proprietà **Name** del cursore dipende dalla relativa forma ed è una delle seguenti: 

    | Forma del cursore     | Nome              |
    |------------------|-------------------|
    | Cursore personalizzato    | Sconosciuto         |
    | \_freccia IDC       | "Normal"          |
    | IDC \_ IBeam       | Modifica            |
    | \_attesa IDC        | Attendere            |
    | IDC \_ incrociato       | Di         |
    | IDC a \_ freccia     | Fino              |
    | IDC \_ SIZENWSE    | "Dimensioni NWSE"       |
    | IDC \_ SIZENESW    | "Dimensioni NESW"       |
    | IDC \_ SIZEWE      | "Dimensioni orizzontali" |
    | IDC \_ SIZENS      | "Dimensioni verticali"   |
    | IDC \_ SIZEALL     | Spostare            |
    | \_No IDC          | Accesso negato       |
    | IDC \_ APPSTARTING | "Avvio dell'app"       |
    | Guida di IDC \_        | Aiuto            |

    

     

-   [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la proprietà **Role** è [**il \_ \_ cursore del sistema Role**](object-roles.md).
-   [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): la proprietà **state** è una combinazione di uno o più dei [valori](object-state-constants.md)seguenti:

    [**Stato \_ di sistema \_**](object-state-constants.md) di stato invisibile al sistema a \| [ **\_ \_ virgola mobile**](object-state-constants.md)

## <a name="notes"></a>Note

-   A differenza di altri elementi dell'interfaccia utente, all'oggetto cursore non è associato un handle di finestra. Per ottenere l'accesso all'oggetto cursore, i client devono impostare un [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) e attendere la generazione di eventi da parte dell'oggetto cursore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




