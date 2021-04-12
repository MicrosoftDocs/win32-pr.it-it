---
title: Metodo ITSRemoteProgram ServerStartProgram
description: Specifica un programma RemoteApp da avviare nella sessione remota.
ms.assetid: 5fb251bf-4832-4e35-b372-23418c280350
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ServerStartProgram
- Metodo ServerStartProgram Servizi Desktop remoto, interfaccia ITSRemoteProgram
- Interfaccia ITSRemoteProgram Servizi Desktop remoto, metodo ServerStartProgram
- Metodo ServerStartProgram Servizi Desktop remoto, interfaccia ITSRemoteProgram2
- Interfaccia ITSRemoteProgram2 Servizi Desktop remoto, metodo ServerStartProgram
- Metodo ServerStartProgram Servizi Desktop remoto, interfaccia ITSRemoteProgram3
- Interfaccia ITSRemoteProgram3 Servizi Desktop remoto, metodo ServerStartProgram
topic_type:
- apiref
api_name:
- ITSRemoteProgram.ServerStartProgram
- ITSRemoteProgram2.ServerStartProgram
- ITSRemoteProgram3.ServerStartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f18917eeb2eb3c60c1a35683b20f7e4604eddde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518045"
---
# <a name="itsremoteprogramserverstartprogram-method"></a>Metodo ITSRemoteProgram:: ServerStartProgram

Specifica un programma RemoteApp da avviare nella sessione remota. Questa funzione deve essere richiamata in una sessione connessa (dopo che la notifica connessa alla sessione viene ricevuta dal client). Un numero qualsiasi di programmi RemoteApp può essere avviato in una sessione. Si verifica il timeout di una sessione RemoteApp se nessun programma RemoteApp viene avviato nella sessione entro il limite di timeout, che è di due minuti per Windows Server 2008.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ServerStartProgram(
  [in] BSTR         bstrExecutablePath,
  [in] BSTR         bstrFilePath,
  [in] BSTR         bstrWorkingDirectory,
  [in] VARIANT_BOOL vbExpandEnvVarInWorkingDirectoryOnServer,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrExecutablePath* \[ in\]
</dt> <dd>

Percorso del file eseguibile del programma RemoteApp nel server.

</dd> <dt>

*bstrFilePath* \[ in\]
</dt> <dd>

Percorso di un file da aprire sul server tramite un'associazione di file, ad esempio "C: \\ \\ documents \\ \\MyReport.docx". Se si specifica *bstrFilePath*, non è necessario specificare il parametro *bstrExecutablePath* e viceversa. È necessario specificare solo uno dei parametri.

</dd> <dt>

*bstrWorkingDirectory* \[ in\]
</dt> <dd>

Directory di lavoro sul server per il programma RemoteApp.

</dd> <dt>

*vbExpandEnvVarInWorkingDirectoryOnServer* \[ in\]
</dt> <dd>

Indica se il server deve espandere le variabili di ambiente nel percorso della directory di lavoro. Impostare questo parametro su **Variant \_ true** se il percorso della directory di lavoro contiene le variabili di ambiente oppure **Variant \_ false** se il percorso della directory di lavoro non contiene variabili di ambiente.

</dd> <dt>

*bstrArguments* \[ in\]
</dt> <dd>

Argomenti della riga di comando per il programma RemoteApp specificati in *bstrExecutablePath*. Impostare su **null** se *bstrExecutablePath* non è specificato.

</dd> <dt>

*vbExpandEnvVarInArgumentsOnServer* \[ in\]
</dt> <dd>

Indica se il server deve espandere le variabili di ambiente negli argomenti della riga di comando. Impostare questo parametro su **Variant \_ true** se gli argomenti contengono variabili di ambiente o **Variant \_ false** se gli argomenti non contengono variabili di ambiente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **\_ OK** se ha esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ ITSRemoteProgram è definito come FDD029F9-467a-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**ITSRemoteProgram**](itsremoteprogram.md)
</dt> </dl>

 

 





