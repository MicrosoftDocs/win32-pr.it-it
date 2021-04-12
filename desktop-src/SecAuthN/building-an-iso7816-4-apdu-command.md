---
description: La procedura seguente fornisce una breve panoramica del processo di compilazione.
ms.assetid: a369d4d7-bd4b-4b4d-846e-ad85251e9ffb
title: Compilazione di un comando ISO7816-4 APDU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63987f27e74dd30b4520e6e09f27ae716d793d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226486"
---
# <a name="building-an-iso7816-4-apdu-command"></a>Compilazione di un comando ISO7816-4 APDU

Per aggiungere funzionalità a un provider di servizi, è necessario capire come viene compilata un' [*unità dati del protocollo*](/windows/desktop/SecGloss/a-gly) ISO7816-4 (APDU) all'interno delle dll del provider di servizi di base. La procedura seguente fornisce una breve panoramica del processo di compilazione.

> [!Note]  
> L'esempio incluso in questo argomento non è necessariamente completo; Per ulteriori informazioni, vedere le applicazioni e le DLL di esempio.

 

**Per compilare un comando ISO7816-4 APDU**

1.  Creare un oggetto [**ISCardCmd**](iscardcmd.md) e un oggetto [**ISCardISO7816**](iscardiso7816.md) .

    ```C++
    //  Create an ISCardCmd object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardCmd,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardCmd,
                               (LPVOID*) &g_pISCardCmd);
    //  Create an ISCardISO7816 object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardISO7816,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardISO7816,
                               (LPVOID*) &g_pISCardISO7816);
    ```

    

    L'interfaccia [**ISCardCmd**](iscardcmd.md) contiene due buffer **IByteBuffer** . Un buffer contiene la stringa di comando APDU effettiva, più tutti i dati da inviare con il comando. L'altra contiene le informazioni di risposta restituite dalla scheda dopo l'esecuzione del comando.

2.  Usando questi oggetti, creare un comando ISO7816-4 valido come segue:

    ```C++
    //  Do challenge.
    HRESULT hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                             &g_pISCardCmd);
    ```

    

    Ecco il codice usato nel metodo [**getchallenge**](iscardiso7816-getchallenge.md) :

    ```C++
    #include <windows.h>

    STDMETHODIMP CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                                IN OUT LPSCARDCMD *ppCmd)
    {
        //  Locals.
        HRESULT hr = S_OK;
        
        try
        {
            //  Is the ISCardCmd object okay?
            hr = IsSCardCmdValid(ppCmd);
            if (FAILED(hr))
                throw (hr);

            //  Do it.
            hr = (*ppCmd)->BuildCmd(m_byClassId,
                                    (BYTE) INS_GET_CHALLENGE,
                                    (BYTE) INS_NULL,  // P1 = 0x00
                                    (BYTE) INS_NULL,  // P2 = 0x00
                                    NULL,
                                    &dwBytesExpected);
            if (FAILED(hr))
                throw (hr);
        }
    }
    ```

    

    Il metodo [**ISCardISO7816:: getchallenge**](iscardiso7816-getchallenge.md) usa il metodo [**ISCardCmd:: BuildCmd**](iscardcmd-buildcmd.md) per compilare la APDU richiesta. Questa operazione viene eseguita scrivendo le informazioni appropriate nel buffer APDU di [**ISCardCmd**](iscardcmd.md) nell'istruzione seguente:

    ```C++
    hr = (*ppCmd)->BuildCmd;
    ```

    

3.  Utilizzando l'oggetto [**ISCardCmd**](iscardcmd.md) compilato, eseguire una transazione con la scheda, interpretare i risultati e continuare.

## <a name="expanding-beyond-iso7816-4"></a>Espansione oltre ISO7816-4

Il metodo consigliato per espandere il processo di compilazione/esecuzione del provider di servizi descritto in precedenza consiste nel creare un nuovo oggetto COM. Questo oggetto COM deve supportare una nuova interfaccia che consente la creazione di comandi non ISO7816-4 e deve aggregare l'interfaccia [**ISCardISO7816**](iscardiso7816.md) .

## <a name="example-of-building-an-iso7816-4-apdu-command"></a>Esempio di compilazione di un comando ISO7816-4 APDU

Nell'esempio seguente viene illustrato il codice utilizzato nella procedura precedente.


```C++
//  Create an ISCardCmd object.
hresult = CoCreateInstance(CLSID_CSCardCmd,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardCmd,
                           (LPVOID*) &g_pISCardCmd);
//  Create an ISCardISO7816 object.
hresult = CoCreateInstance(CLSID_CSCardISO7816,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardISO7816,
                           (LPVOID*) &g_pISCardISO7816);
//  Do challenge.
hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                         &g_pISCardCmd);

STDMETHODIMP
CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                            IN OUT LPSCARDCMD *ppCmd)
{
    //  Locals.
    HRESULT hr = S_OK;
    
    try
    {
        //  Is the ISCardCmd object okay?
        hr = IsSCardCmdValid(ppCmd);
        if (FAILED(hr))
            throw (hr);

        //  Do it.
        hr = (*ppCmd)->BuildCmd(m_byClassId,
                                (BYTE) INS_GET_CHALLENGE,
                                (BYTE) INS_NULL,  // P1 = 0x00
                                (BYTE) INS_NULL,  // P2 = 0x00
                                NULL,
                                &dwBytesExpected);
        if (FAILED(hr))
            throw (hr);
    }
}
```



 

 
