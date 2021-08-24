---
title: Per identificare gli input in base al numero
description: Per identificare gli input in base al numero
ms.assetid: f468f74d-7eed-4819-957d-241903f44d2d
keywords:
- Advanced Systems Format (ASF), identificazione degli input in base al numero
- ASF (Advanced Systems Format), identificazione degli input in base al numero
- profili, identificazione degli input in base al numero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ff09a81cac98edc6f14ded98ba9852501bfdfef4c5e40affa908c0ff710e1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807531"
---
# <a name="to-identify-inputs-by-number"></a>Per identificare gli input in base al numero

Ogni esempio passato al writer deve essere associato a un numero di input. Ogni numero di input corrisponde a uno o più flussi nel profilo utilizzato dal writer per scrivere il file. In un profilo le origini multimediali sono identificate da un nome di connessione. Il writer associa un numero di input a ogni nome di connessione quando si imposta il profilo per il writer. Prima di poter passare esempi al writer, è necessario determinare i dati che ogni input prevede. Non è possibile presupporre che gli input siano nello stesso ordine dei flussi in un profilo, anche se questo è spesso il caso. Pertanto, l'unico modo affidabile per trovare la corrispondenza degli input con i flussi è confrontare il nome della connessione dell'input con il nome della connessione del flusso.

Per identificare i nomi di connessione e i numeri di input corrispondenti per un profilo caricato, seguire questa procedura:

1.  Creare un oggetto writer e impostare un profilo da usare. Per altre informazioni sull'impostazione dei profili nel writer, vedere [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md). È necessario conoscere i nomi di connessione usati per i flussi nel profilo. È possibile ottenere il nome della connessione dall'interno del profilo ottenendo l'oggetto di configurazione del flusso per ogni flusso e chiamando [**IWMStreamConfig::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname). Per altre informazioni sui profili e sugli oggetti di configurazione del flusso, vedere [Utilizzo dei profili.](working-with-profiles.md)
2.  Recuperare il numero totale di input chiamando [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount).
3.  Scorrere tutti gli input, eseguendo i passaggi seguenti per ognuno.
    -   Recuperare [**l'interfaccia IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) per l'input chiamando [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).
    -   Recuperare il nome della connessione che corrisponde al numero di input chiamando [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname). Dopo aver creato il nome della connessione, si conoscono i flussi associati ai numeri di input assegnati dal writer.

Nell'esempio di codice seguente viene visualizzato il nome della connessione per ogni input. Per altre informazioni sull'uso di questo codice, vedere [Uso degli esempi di codice.](using-the-code-examples.md)


```C++
HRESULT GetNamesForInputs(IWMWriter* pWriter)
{
    DWORD    cInputs  = 0;
    HRESULT  hr       = S_OK;
    WCHAR*   pwszName = NULL;
    WORD     cchName  = 0;

    IWMInputMediaProps* pProps = NULL;

    // Get the total number of inputs for the file.
    hr = pWriter->GetInputCount(&cInputs);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all supported inputs.
    for (DWORD inputIndex = 0; inputIndex < cInputs; inputIndex++)
    {
        // Get the input properties for the input.
        hr = pWriter->GetInputProps(inputIndex, &pProps);  
        GOTO_EXIT_IF_FAILED(hr);

        // Get the size of the connection name.
        hr = pProps->GetConnectionName(0, &cchName);
        GOTO_EXIT_IF_FAILED(hr);

        if (cchName > 0)
        {
            // Allocate memory for the connection name.
            pwszName = new WCHAR[cchName];
            if (wszName == NULL)
            {
                hr = E_OUTOFMEMORY;
                goto Exit;
            }

            // Get the connection name.
            hr = pProps->GetConnectionName(pwszName, &cchName);
            GOTO_EXIT_IF_FAILED(hr);
            
            // Display the name.
            printf("Input # %d = %S\n", pwszName);
        } // end if

        // Clean up for next iteration.
        SAFE_ARRAY_DELETE(pwszName);
        SAFE_RELEASE(pProps);
    } // end for inputIndex

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_RELEASE(pProps);
    return hr;
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




