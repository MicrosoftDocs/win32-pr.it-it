---
description: Il modello di sicurezza di Windows consente di controllare l'accesso agli oggetti di mapping di file. Per ulteriori informazioni, vedere Access-Control Model.
ms.assetid: 8bbf7c98-ff83-4ed9-8b82-f08dcd31295c
title: Diritti di accesso e sicurezza per il mapping dei file
ms.topic: article
ms.date: 10/06/2018
ms.openlocfilehash: 65d520e12d1b555e7c633f0d1e0ba5142c330ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306583"
---
# <a name="file-mapping-security-and-access-rights"></a>Diritti di accesso e sicurezza per il mapping di file

Il modello di sicurezza di Windows consente di controllare l'accesso agli oggetti di mapping di file. Per altre informazioni, vedere [modello di controllo di accesso](../secauthz/access-control-model.md).

È possibile specificare un [descrittore di sicurezza](../secauthz/security-descriptors.md) per un oggetto mapping di file quando si chiama la funzione [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) . Se si specifica **null**, l'oggetto ottiene un descrittore di sicurezza predefinito. Gli ACL nel descrittore di sicurezza predefinito per un oggetto di mapping dei file provengono dal token primario o di rappresentazione del creatore.

Per recuperare il descrittore di sicurezza di un oggetto mapping di file, chiamare la funzione [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa) o [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo) . Per impostare il descrittore di sicurezza di un oggetto mapping di file, chiamare la funzione [**SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa) o [**SetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) .

I diritti di accesso validi per gli oggetti di mapping dei file includono i [diritti di accesso di tipo](../secauthz/standard-access-rights.md) **eliminazione**, **lettura \_** e **scrittura \_ e scrittura** del **\_ proprietario** . Gli oggetti di mapping dei file non supportano il diritto di accesso standard di **sincronizzazione** . Nella tabella seguente sono elencati i diritti di accesso specifici per gli oggetti di mapping di file.

| Diritto di accesso | Significato |
|-|-|
| **\_accesso a \_ tutti i file mappa \_** | Include tutti i diritti di accesso a un oggetto di mapping di file ad eccezione di **\_ \_ Esegui mapping file**. Le funzioni [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) e [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) considerano questo oggetto analogo a quanto specificato per la **\_ \_ scrittura di mapping di file**. |
| **\_esecuzione mapping di file \_** | Consente il mapping di viste eseguibili dell'oggetto mapping di file. L'oggetto deve essere stato creato con la protezione della pagina che consente l'accesso in esecuzione, ad esempio **pagina \_ esecuzione \_ lettura**, **pagina \_ esecuzione \_ WRITECOPY** o **pagina \_ esecuzione \_ ReadWrite** protezione.  |
| **\_lettura mapping \_ file** | Consente il mapping delle visualizzazioni di sola lettura o copy-on-Write dell'oggetto mapping di file.  |
| **\_scrittura mappa \_ file** | Consente il mapping delle visualizzazioni di sola lettura, copia in scrittura o lettura/scrittura di un oggetto mapping di file. L'oggetto deve essere stato creato con la protezione della pagina che consente l'accesso in scrittura, ad esempio **pagina \_ ReadWrite** o **pagina \_ esecuzione \_ ReadWrite** protezione. |

Il mapping di una visualizzazione copy-on-Write di un oggetto mapping di file richiede lo stesso accesso come mapping di una visualizzazione di sola lettura. Il flag di **\_ \_ copia della mappa file** non è un diritto di accesso e non deve essere specificato come parte di un DACL in un descrittore di sicurezza. Questo valore può essere usato solo con funzioni che mappano una visualizzazione di un oggetto mapping di file, ad esempio le funzioni [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) e [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) , o con la funzione [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) , che considera la **\_ \_ copia** del mapping dei file nello stesso modo in cui tratta la **lettura della \_ mappa \_ del file**.

È possibile richiedere il diritto di accesso di **\_ \_ sicurezza del sistema di accesso** a un oggetto mapping di file se si desidera leggere o scrivere il SACL dell'oggetto. Per altre informazioni, vedere [elenchi di controllo di accesso (ACL)](../secauthz/access-control-lists.md) e [accesso SACL diritto](../secauthz/sacl-access-right.md).
