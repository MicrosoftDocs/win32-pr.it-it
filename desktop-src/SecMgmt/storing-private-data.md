---
description: I criteri LSA forniscono due funzioni che è possibile usare per impostare e recuperare dati privati.
ms.assetid: 7b6e63d4-ce8f-4279-85d9-da6b2b589afa
title: Archiviazione di dati privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bfb1d9a701a93a125d68f81d7f487ffc2e2c7a337fa6bec0276086c08ffabc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118893438"
---
# <a name="storing-private-data"></a>Archiviazione di dati privati

I criteri LSA forniscono due funzioni che è possibile usare per impostare e recuperare dati privati. Questi dati vengono archiviati come stringa crittografata nel Registro di sistema. Ad esempio, è possibile usare queste funzioni per archiviare le password degli account server e altre informazioni riservate.

Chiamare la [**funzione LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) per archiviare e crittografare i dati privati. Come descritto in [Private Data Object](private-data-object.md), gli oggetti dati privati includono tre tipi specializzati: local, global e machine. Per creare un oggetto specializzato, aggiungere un prefisso al nome della chiave passato a **LsaStorePrivateData:**"L$" per gli oggetti locali, "G$" per gli oggetti globali e "M$" per gli oggetti computer. Se non si crea uno di questi tipi specializzati, non è necessario specificare un prefisso del nome di chiave.

Per recuperare e decodificare i dati privati archiviati in [**precedenza, chiamare LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata). Si noti che non è possibile recuperare oggetti dati privati del computer. Gli oggetti computer possono essere recuperati solo dal sistema operativo.

Prima di poter archiviare o recuperare dati privati, l'applicazione deve ottenere un handle per l'oggetto [**Criteri**](policy-object.md) locale, come illustrato in Apertura di un handle [di oggetto criteri.](opening-a-policy-object-handle.md)

Nell'esempio seguente viene creato un oggetto dati privato locale. Si noti che la funzione InitLsaString converte una stringa [*Unicode*](/windows/desktop/SecGloss/u-gly) in una [**struttura LSA \_ UNICODE \_ STRING.**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) Il codice per questa funzione è illustrato in [Uso di stringhe Unicode LSA.](using-lsa-unicode-strings.md)


```C++
#include <windows.h>
#include <stdio.h>

BOOL CreatePrivateDataObject(LSA_HANDLE PolicyHandle)
{
  NTSTATUS ntsResult;
  LSA_UNICODE_STRING lucKeyName;
  LSA_UNICODE_STRING lucPrivateData;
  // The L$ prefix specifies a local private data object
  WCHAR wszKeyName[] = L"L$MyPrivateKey";
  WCHAR wszPrivateData[] = L"Something secret.";

  // Initializing PLSA_UNICODE_STRING structures
  if (!InitLsaString(&lucKeyName, wszKeyName))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }
  if (!InitLsaString(&lucPrivateData, wszPrivateData))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }

  // Store the private data.
  ntsResult = LsaStorePrivateData(
    PolicyHandle,   // handle to a Policy object
    &lucKeyName,    // key to identify the data
    &lucPrivateData // the private data
  );
  if (ntsResult != STATUS_SUCCESS)
  {
    wprintf(L"Store private object failed %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return FALSE;
  }
  return TRUE;
}
```



> [!Note]  
> I dati archiviati dalla [**funzione LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) non sono assolutamente protetti. La chiave, tuttavia, dispone di [*un*](/windows/desktop/SecGloss/d-gly) elenco di controllo di accesso discrezionale (DACL) che consente solo all'autore e agli amministratori di leggere i dati.

 

 

 
