---
description: A ogni oggetto Active Directory è assegnato un descrittore di sicurezza.
ms.assetid: 2e4ed13f-f09e-43b4-9862-95a79c229f0c
title: Diritti di accesso ai servizi directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f24e75db6733a8f5833e7f45ab5a52dafd67f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233697"
---
# <a name="directory-services-access-rights"></a>Diritti di accesso ai servizi directory

A ogni oggetto Active Directory è assegnato un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) . All'interno di questi descrittori di sicurezza è possibile impostare un set di diritti fiduciari specifici per gli oggetti del servizio directory. Questi diritti sono elencati nella tabella seguente. Per altre informazioni, vedere [controllare i diritti di accesso](/windows/desktop/AD/control-access-rights).



| Diritti                                | Significato                                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTRL \_ DS \_ aperto<br/>            | Aprire un oggetto DS.<br/>                                                                                                                                                                                                                                                            |
| \_ \_ creazione \_ figlio di ACTRL DS<br/>   | Creare un oggetto DS figlio.<br/>                                                                                                                                                                                                                                                    |
| \_ \_ eliminazione figlio ACTRL \_ DS<br/>   | Eliminare un oggetto DS figlio.<br/>                                                                                                                                                                                                                                                    |
| elenco di ACTRL \_ DS \_<br/>            | Enumerare un oggetto DS.<br/>                                                                                                                                                                                                                                                       |
| ACTRL \_ DS \_ Read \_ prop<br/>      | Leggere le proprietà di un oggetto DS.<br/>                                                                                                                                                                                                                                          |
| ACTRL \_ DS \_ Write \_ prop<br/>     | Scrivere le proprietà per un oggetto DS.<br/>                                                                                                                                                                                                                                            |
| \_self ACTRL DS \_<br/>            | L'accesso consentito solo dopo i controlli dei diritti convalidati supportati dall'oggetto viene eseguito. Questo flag può essere usato da solo per eseguire tutti i controlli dei diritti convalidati dell'oggetto o può essere combinato con un identificatore di un diritto convalidato specifico per eseguire solo quel controllo.<br/> |
| \_ \_ albero eliminazione ACTRL \_ DS<br/>    | Eliminare una struttura ad albero di oggetti DS.<br/>                                                                                                                                                                                                                                                 |
| \_ \_ oggetto elenco DS \_ ACTRL<br/>    | Elencare un albero di oggetti DS.<br/>                                                                                                                                                                                                                                                   |
| \_ \_ accesso al controllo DS ACTRL \_<br/> | L'accesso consentito solo dopo la verifica dei diritti estesi supportati dall'oggetto viene eseguito. Questo flag può essere usato da solo per eseguire tutti i controlli dei diritti estesi sull'oggetto oppure può essere combinato con un identificatore di un diritto esteso specifico per eseguire solo quel controllo.<br/>    |



 

 

