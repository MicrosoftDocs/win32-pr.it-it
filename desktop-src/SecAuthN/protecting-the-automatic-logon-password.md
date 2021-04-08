---
description: La password di accesso automatico deve essere protetta tramite la funzione LsaStorePrivateData.
ms.assetid: 7bd4d725-de17-4801-bd06-8d47a777409d
title: Protezione della password di accesso automatico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25508af4de64554e664426db3e786a1eca34579b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968227"
---
# <a name="protecting-the-automatic-logon-password"></a>Protezione della password di accesso automatico

La password di accesso automatico deve essere protetta tramite la funzione [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) .

Nell'esempio seguente viene illustrato come proteggere la password di accesso automatico. Nell'esempio viene recuperato un handle per l'oggetto [**policy**](../secmgmt/policy-object.md) chiamando la funzione [**LsaOpenPolicy**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopenpolicy) . Per ulteriori informazioni sull'oggetto **criteri e sugli handle degli oggetti** **criteri** , vedere rispettivamente oggetto **criteri** e [apertura di un handle di oggetto Criteri](../secmgmt/opening-a-policy-object-handle.md). Nell'esempio viene quindi impostata la password protetta chiamando la funzione [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) . Si noti che se il chiamante passa **null** come valore della password protetta, il codice Cancella la password protetta esistente. Prima di uscire, il codice chiude l'handle all'oggetto **criterio** .


```C++
#include <windows.h>
#include <stdio.h>

DWORD UpdateDefaultPassword(WCHAR * pwszSecret)
{

    LSA_OBJECT_ATTRIBUTES ObjectAttributes;
    LSA_HANDLE LsaPolicyHandle = NULL;

    LSA_UNICODE_STRING lusSecretName;
    LSA_UNICODE_STRING lusSecretData;
    USHORT SecretNameLength;
    USHORT SecretDataLength;

    NTSTATUS ntsResult = STATUS_SUCCESS;
    DWORD dwRetCode = ERROR_SUCCESS;

    //  Object attributes are reserved, so initialize to zeros.
    ZeroMemory(&ObjectAttributes, sizeof(ObjectAttributes));

    //  Get a handle to the Policy object.
    ntsResult = LsaOpenPolicy(
        NULL,    // local machine
        &ObjectAttributes, 
        POLICY_CREATE_SECRET,
        &LsaPolicyHandle);

    if( STATUS_SUCCESS != ntsResult )
    {
        //  An error occurred. Display it as a win32 error code.
        dwRetCode = LsaNtStatusToWinError(ntsResult);
        wprintf(L"Failed call to LsaOpenPolicy %lu\n", dwRetCode);
        return dwRetCode;
    } 

    //  Initialize an LSA_UNICODE_STRING for the name of the
    //  private data ("DefaultPassword").
    SecretNameLength = (USHORT)wcslen(L"DefaultPassword");
    lusSecretName.Buffer = L"DefaultPassword";
    lusSecretName.Length = SecretNameLength * sizeof(WCHAR);
    lusSecretName.MaximumLength =
        (SecretNameLength+1) * sizeof(WCHAR);

    //  If the pwszSecret parameter is NULL, then clear the secret.
    if( NULL == pwszSecret )
    {
        wprintf(L"Clearing the secret...\n");
        ntsResult = LsaStorePrivateData(
            LsaPolicyHandle,
            &lusSecretName,
            NULL);
        dwRetCode = LsaNtStatusToWinError(ntsResult);
    }
    else
    {
        wprintf(L"Setting the secret...\n");
        //  Initialize an LSA_UNICODE_STRING for the value
        //  of the private data. 
        SecretDataLength = (USHORT)wcslen(pwszSecret);
        lusSecretData.Buffer = pwszSecret;
        lusSecretData.Length = SecretDataLength * sizeof(WCHAR);
        lusSecretData.MaximumLength =
            (SecretDataLength+1) * sizeof(WCHAR);
        ntsResult = LsaStorePrivateData(
            LsaPolicyHandle,
            &lusSecretName,
            &lusSecretData);
        dwRetCode = LsaNtStatusToWinError(ntsResult);
    }

    LsaClose(LsaPolicyHandle);

    if (dwRetCode != ERROR_SUCCESS)
        wprintf(L"Failed call to LsaStorePrivateData %lu\n",
            dwRetCode);
    
    return dwRetCode;

}

```



Si noti che se Winlogon non trova una password archiviata dalla funzione [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) , userà il valore **DefaultPassword** della chiave Winlogon (se esistente) per la password di accesso automatico.

Per ulteriori informazioni sull'accesso automatico e sulla chiave del registro di sistema Winlogon, vedere [MSGina.dll funzionalità](msgina-dll-features.md).

Per ulteriori informazioni sulla protezione delle password, vedere [gestione delle password](../secbp/handling-passwords.md).

 

 
