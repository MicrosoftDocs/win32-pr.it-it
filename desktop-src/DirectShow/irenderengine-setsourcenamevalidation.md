---
description: Il metodo SetSourceNameValidation specifica il modo in cui il motore di rendering convalida i nomi di file.
ms.assetid: b33904cd-ed7d-41b5-9ebf-50983ec9f7b3
title: 'Metodo IRenderEngine:: SetSourceNameValidation (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetSourceNameValidation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 96164a817fd04f505b32c17be1bff3268e847df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330782"
---
# <a name="irenderenginesetsourcenamevalidation-method"></a>Metodo IRenderEngine:: SetSourceNameValidation

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetSourceNameValidation` metodo specifica il modo in cui il motore di rendering convalida i nomi di file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSourceNameValidation(
   BSTR          FilterString,
   IMediaLocator *pOverride,
   LONG          Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FilterString* 
</dt> <dd>

Valore **BSTR** contenente coppie di stringhe di filtro, formattato come richiesto dal membro **LpstrFilter** della struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) . Il localizzatore multimediale usa questo filtro se presenta una finestra di dialogo Apri file per l'utente finale.

</dd> <dt>

*pOverride* 
</dt> <dd>

Puntatore facoltativo all'interfaccia [**IMediaLocator**](imedialocator.md) di un localizzatore multimediale da usare al posto del valore predefinito. Per usare il localizzatore multimediale predefinito, impostare il valore di questo parametro su **null**. Per ulteriori informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*Flag* 
</dt> <dd>

Combinazione bit per bit dei [**flag di convalida dei nomi di file**](file-name-validation-flags.md) che specificano il comportamento del localizzatore multimediale. Il \_ flag di controllo SFN VALIDATEF \_ deve essere presente. Il \_ flag SFN VALIDATEF \_ hlinkMUTED non ha alcun effetto con questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** :



| Codice restituito                                                                                            | Descrizione                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Esito positivo.<br/>                            |
| <dl> <dt>**E \_ deve \_ inizializzare il \_ RENDERER**</dt> </dl> | Impossibile inizializzare il motore di rendering.<br/> |



 

## <a name="remarks"></a>Commenti

Utilizzando il parametro *pOverride* , è possibile fornire un'implementazione personalizzata dell'interfaccia [**IMediaLocator**](imedialocator.md) . Ad esempio, il localizzatore multimediale predefinito non notifica a un'applicazione i file che trova (o non trova). Per aggirare questa limitazione, è possibile implementare un localizzatore multimediale personalizzato, rendendolo un wrapper per la versione predefinita. Passare quindi le chiamate a [**IMediaLocator:: FindMediaFile**](imedialocator-findmediafile.md) direttamente alla versione predefinita ed esaminare il valore restituito.

Attualmente, questo metodo non convalida le origini caricate dinamicamente. Vedere [**IRenderEngine:: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IRenderEngine**](irenderengine.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 
