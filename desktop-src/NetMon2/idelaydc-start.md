---
description: Il metodo Start avvia un'acquisizione.
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: 'Metodo IDelaydC:: Start (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a912af44dddb8a25d3279a5cdd7f021646c26e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305882"
---
# <a name="idelaydcstart-method"></a>Metodo IDelaydC:: Start

Il metodo **Start** avvia un'acquisizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFileName* \[ out\]
</dt> <dd>

Puntatore al nome del file di [*acquisizione*](c.md) usato per archiviare i dati di rete. Assicurarsi di memorizzare nella cache il nome del file, se necessario, per riferimento futuro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                           | Descrizione                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_acquisizione NMERR \_ sospesa**</dt> </dl> | L'acquisizione si trova in uno stato di sospensione e deve essere arrestata prima di poter essere riavviata. Chiamare [**IDelaydC:: Stop**](idelaydc-stop.md) per arrestare l'acquisizione. Per ulteriori informazioni, vedere la sezione Osservazioni in questo argomento.<br/> |
| <dl> <dt>**\_acquisizione NMERR**</dt> </dl>       | Acquisizione già avviata.<br/>                                                                                                                                                                                 |
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl>  | L'oggetto NPP non è connesso alla rete. Chiamare [**IDelaydC:: Connect**](idelaydc-connect.md) per connettersi alla rete.<br/>                                                                                          |
| <dl> <dt>**NMERR \_ non \_ ritardato**</dt> </dl>    | L'oggetto NPP è connesso alla rete, ma non con il metodo [**IDelaydC:: Connect**](idelaydc-connect.md) .<br/>                                                                                                      |



 

## <a name="remarks"></a>Commenti

Il percorso del [*file di acquisizione*](c.md) è specificato nel registro di sistema di Windows, ma è possibile usare Network Monitor per modificare il percorso del file.

Per riavviare l'acquisizione usando **IDelaydC:: Start** e [**IDelaydC:: Stop**](idelaydc-stop.md), è necessario chiamare il metodo [**IDelaydC:: Configure**](idelaydc-configure.md) per riconfigurare la connessione ogni volta che si chiama il metodo **IDelaydC:: Start** per riavviare l'acquisizione dei dati. Quando si avvia e si arresta l'acquisizione con questi tre metodi, viene creato un nuovo file di acquisizione ogni volta che viene avviata l'acquisizione.

> [!Note]  
> È anche possibile avviare e arrestare l'acquisizione usando i metodi [**IDelaydC::P ause**](idelaydc-pause.md) e [**IDelaydC:: Resume**](idelaydc-resume.md) . Quando si usano questi due metodi, i dati acquisiti vengono archiviati nello stesso file di acquisizione.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[**IDelaydC:: Configure**](idelaydc-configure.md)
</dt> <dt>

[**IDelaydC:: Connect**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC:: Resume**](idelaydc-resume.md)
</dt> <dt>

[**IDelaydC:: Stop**](idelaydc-stop.md)
</dt> </dl>

 

 




