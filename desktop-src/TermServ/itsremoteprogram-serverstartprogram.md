---
title: Metodo ITSRemoteProgram ServerStartProgram
description: Specifica un programma RemoteApp da avviare nella sessione remota.
ms.assetid: 5fb251bf-4832-4e35-b372-23418c280350
ms.tgt_platform: multiple
keywords:
- Metodo ServerStartProgram Servizi Desktop remoto
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
ms.openlocfilehash: c789a9963086128e93546415247cfb3db69afe59c67a445b851ee5cf3687d16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756857"
---
# <a name="itsremoteprogramserverstartprogram-method"></a>Metodo ITSRemoteProgram::ServerStartProgram

Specifica un programma RemoteApp da avviare nella sessione remota. Questa funzione deve essere richiamata in una sessione connessa (dopo la ricezione della notifica di connessione della sessione nel client). Un numero qualsiasi di programmi RemoteApp può essere avviato in una sessione. Si verifica il timeout di una sessione di RemoteApp se non viene avviato alcun programma RemoteApp nella sessione entro il limite di timeout, ovvero due minuti per Windows Server 2008.

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

*bstrExecutablePath* \[ Pollici\]
</dt> <dd>

Percorso del file eseguibile del programma RemoteApp nel server.

</dd> <dt>

*bstrFilePath* \[ Pollici\]
</dt> <dd>

Percorso di un file da aprire nel server tramite un'associazione di file, ad esempio "C: \\ \\ Documents \\ \\MyReport.docx". Se si specifica *bstrFilePath*, non è necessario specificare il *parametro bstrExecutablePath* e viceversa. È necessario specificare solo uno dei parametri.

</dd> <dt>

*bstrWorkingDirectory* \[ Pollici\]
</dt> <dd>

Directory di lavoro nel server per il programma RemoteApp.

</dd> <dt>

*vbExpandEnvVarInWorkingDirectoryOnServer* \[ Pollici\]
</dt> <dd>

Indica se il server deve espandere le variabili di ambiente nel percorso della directory di lavoro. Impostare questo parametro su **VARIANT \_ TRUE se** il percorso della directory di lavoro contiene variabili di ambiente oppure su VARIANT **\_ FALSE** se il percorso della directory di lavoro non contiene variabili di ambiente.

</dd> <dt>

*bstrArguments* \[ Pollici\]
</dt> <dd>

Argomenti della riga di comando per il programma RemoteApp specificati in *bstrExecutablePath*. Impostare questa proprietà **su NULL** se *bstrExecutablePath* non è specificato.

</dd> <dt>

*vbExpandEnvVarInArgumentsOnServer* \[ Pollici\]
</dt> <dd>

Indica se il server deve espandere le variabili di ambiente negli argomenti della riga di comando. Impostare questo parametro su **VARIANT \_ TRUE se** gli argomenti contengono variabili di ambiente oppure SU VARIANT **\_ FALSE** se gli argomenti non contengono variabili di ambiente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ ITSRemoteProgram è definito come FDD029F9-467A-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**ITSRemoteProgram**](itsremoteprogram.md)
</dt> </dl>

 

 





