---
description: PNRP utilizza la funzione WSALookupServiceEnd per eseguire le operazioni seguenti.
ms.assetid: 0732929e-ca03-438f-80d9-48a3da0095f7
title: PNRP e WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db499c9a736e26d630b623a29baa4c18dcfceeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314741"
---
# <a name="pnrp-and-wsalookupserviceend"></a>PNRP e WSALookupServiceEnd

PNRP utilizza la funzione [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) per eseguire le operazioni seguenti:

-   Termina una query avviata in una chiamata precedente a [ **WSALookupServiceBegin**](winsock-nsp-reference-links.md)
-   Sbloccare una chiamata a [**WSALookupServiceNext**](winsock-nsp-reference-links.md) per arrestare la ricerca

Una chiamata a [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) termina una query e pulisce il contesto. L'handle ottenuto da una chiamata a **WSALookupServiceBegin** deve essere passato come parametro a **WSALookupServiceEnd**.

Per ulteriori informazioni su PNRP e la funzione [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) , vedere [PNRP e WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[PNRP e WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[Codici di errore PNRP NSP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSALookupServiceNext**](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



