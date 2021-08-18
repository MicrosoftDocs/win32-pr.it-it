---
description: La maggior parte delle funzioni criteri LSA richiede un handle per l'oggetto Criteri per il sistema per eseguire query o modificare. Per ottenere un handle per un oggetto Policy, chiamare LsaOpenPolicy e specificare il nome del sistema a cui si vuole accedere e il set di autorizzazioni di accesso necessarie.
ms.assetid: 66fdc878-d9c4-421c-b79f-9df08984611c
title: Apertura di un handle di oggetto criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16baf2cf7e722faca1f0441505ec325b8e64c8aad95522e697b4905f566985af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894052"
---
# <a name="opening-a-policy-object-handle"></a>Apertura di un handle di oggetto criteri

La maggior parte delle funzioni criteri LSA richiede un handle per [**l'oggetto Criteri**](policy-object.md) per il sistema per eseguire query o modificare. Per ottenere un handle per un **oggetto Policy,** chiamare [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) e specificare il nome del sistema a cui si vuole accedere e il set di autorizzazioni di accesso necessarie.

Le autorizzazioni di accesso necessarie per l'applicazione dipendono dalle azioni eseguite. Per informazioni dettagliate sulle autorizzazioni necessarie per ogni funzione, vedere la descrizione di tale funzione in [Funzioni dei criteri LSA.](management-functions.md)

Se la chiamata a [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) ha esito positivo, restituisce un handle [**all'oggetto Policy**](policy-object.md) per il sistema specificato. L'applicazione passa quindi questo handle nelle chiamate di funzione criteri LSA successive. Quando l'applicazione non necessita più dell'handle, deve chiamare [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) per liberarlo.

Nell'esempio seguente viene illustrato come aprire un handle [**di**](policy-object.md) oggetto Policy.


```C++
#include <windows.h>

#define TARGET_SYSTEM_NAME L"mysystem"

LSA_HANDLE GetPolicyHandle()
{
  LSA_OBJECT_ATTRIBUTES ObjectAttributes;
  WCHAR SystemName[] = TARGET_SYSTEM_NAME;
  USHORT SystemNameLength;
  LSA_UNICODE_STRING lusSystemName;
  NTSTATUS ntsResult;
  LSA_HANDLE lsahPolicyHandle;

  // Object attributes are reserved, so initialize to zeros.
  ZeroMemory(&ObjectAttributes, sizeof(ObjectAttributes));

  //Initialize an LSA_UNICODE_STRING to the server name.
  SystemNameLength = wcslen(SystemName);
  lusSystemName.Buffer = SystemName;
  lusSystemName.Length = SystemNameLength * sizeof(WCHAR);
  lusSystemName.MaximumLength = (SystemNameLength+1) * sizeof(WCHAR);

  // Get a handle to the Policy object.
  ntsResult = LsaOpenPolicy(
        &lusSystemName,    //Name of the target system.
        &ObjectAttributes, //Object attributes.
        POLICY_ALL_ACCESS, //Desired access permissions.
        &lsahPolicyHandle  //Receives the policy handle.
    );

  if (ntsResult != STATUS_SUCCESS)
  {
    // An error occurred. Display it as a win32 error code.
    wprintf(L"OpenPolicy returned %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return NULL;
  } 
  return lsahPolicyHandle;
}
```



Nell'esempio precedente l'applicazione ha richiesto i privilegi POLICY \_ ALL \_ ACCESS [](/windows/desktop/SecGloss/p-gly). Per informazioni dettagliate sulle autorizzazioni che l'applicazione deve richiedere quando chiama [**LsaOpenPolicy,**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)vedere le descrizioni delle funzioni a cui l'applicazione passerà l'handle [**dell'oggetto**](policy-object.md) Policy.

Per aprire un handle per l'oggetto [**Policy**](policy-object.md) di un dominio trusted, chiamare [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) (per creare una nuova relazione di trust con un dominio) o [**chiamare LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) (per accedere a un dominio trusted esistente). Entrambe queste funzioni impostano un puntatore a [**un \_ handle LSA**](lsa-handle.md), che è quindi possibile specificare nelle chiamate di funzione di criteri LSA successive. Come per [**LsaOpenPolicy,**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)l'applicazione deve chiamare [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) quando non è più necessario l'handle per l'oggetto **Policy del dominio** trusted.

 

 
