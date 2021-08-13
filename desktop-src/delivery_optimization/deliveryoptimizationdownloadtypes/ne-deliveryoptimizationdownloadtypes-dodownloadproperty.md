---
title: Enumerazione DODownloadProperty
description: Specifica l'ID delle proprietà per l'operazione di download do.
keywords:
- Enumerazione DODownloadProperty, DODownloadProperty
topic_type:
- apiref
api_name:
- DODownloadProperty
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 2e36dc783a7b2c7da23f4513f198b7871f97fe6576f60ffdd6f0fcbd7a11e3f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544577"
---
# <a name="dodownloadproperty-enumeration"></a>Enumerazione DODownloadProperty

**L'enumerazione DODownloadProperty** specifica l'ID delle proprietà per l'operazione di download do. Questa enumerazione viene utilizzata **dall'interfaccia IDODownload** ed eseguita da un valore VARIANT, in cui è contenuto il tipo di valore.

## <a name="syntax"></a>Sintassi

```cpp
typedef enum _DODownloadProperty
{
  DODownloadProperty_Id = 0,
  DODownloadProperty_Uri,
  DODownloadProperty_ContentId,
  DODownloadProperty_DisplayName,
  DODownloadProperty_LocalPath,
  DODownloadProperty_HttpCustomHeaders,
  DODownloadProperty_CostPolicy,
  DODownloadProperty_SecurityFlags,
  DODownloadProperty_CallbackFreqPercent,
  DODownloadProperty_CallbackFreqSeconds,
  DODownloadProperty_NoProgressTimeoutSeconds,
  DODownloadProperty_ForegroundPriority,
  DODownloadProperty_BlockingMode,
  DODownloadProperty_CallbackInterface,
  DODownloadProperty_StreamInterface,
  DODownloadProperty_SecurityContext,
  DODownloadProperty_NetworkToken
  DODownloadProperty_CorrelationVector,
  DODownloadProperty_DecryptionInfo,
  DODownloadProperty_IntegrityCheckInfo,
  DODownloadProperty_IntegrityCheckMandatory,
  DODownloadProperty_TotalSizeBytes
} DODownloadProperty;
```

## <a name="constants"></a>Costanti

| Requisito | Valore |
|-|-|
| DODownloadProperty_Id | Di sola lettura. Usare questa proprietà per ottenere l'ID che identifica in modo univoco il download. Il tipo VARIANT è VT_BSTR. |
| DODownloadProperty_Uri | Usare questa proprietà per impostare o ottenere il percorso URI remoto della risorsa da scaricare. Questa proprietà è obbligatoria solo *se DODownloadProperty_ContentId* non viene specificata. Il tipo VARIANT è VT_BSTR. |
| DODownloadProperty_ContentId | Usare questa proprietà per impostare o ottenere l'ID contenuto univoco del download. Questa proprietà è obbligatoria solo *se DODownloadProperty_Uri* non viene specificato. Il tipo VARIANT è VT_BSTR. |
| DODownloadProperty_DisplayName | facoltativo. Usare questa proprietà per impostare o ottenere il nome visualizzato del download. Il tipo VARIANT è VT_BSTR. |
| DODownloadProperty_LocalPath | Usare questa proprietà per impostare o ottenere il nome del percorso locale per salvare il file di download. Se il percorso non esiste, DO tenterà di crearlo con i privilegi del chiamante. Questa proprietà è obbligatoria solo *se DODownloadProperty_StreamInterface* non è stata specificata. Il tipo VARIANT è VT_BSTR. |
| DODownloadProperty_HttpCustomHeaders | facoltativo. Usare questa proprietà per impostare o ottenere intestazioni di richiesta HTTP personalizzate. DO includerà queste intestazioni durante le operazioni di richiesta di file HTTP. Le intestazioni devono essere già formattate come intestazioni HTTP standard. Il tipo VARIANT è VT_BSTR. |
| DODownloadProperty_CostPolicy | facoltativo. Usare questa proprietà per impostare o ottenere uno dei valori di **enumerazione DODownloadCostPolicy.** Il tipo VARIANT è VT_UI4. |
| DODownloadProperty_SecurityFlags | Facoltativo di sola scrittura. Usare questa proprietà per impostare o ottenere i flag di sicurezza WinHTTP standard (**WINHTTP_OPTION_SECURITY_FLAGS**). Il tipo VARIANT è VT_UI4.</br></br>Sono supportati i flag seguenti:</br>SECURITY_FLAG_IGNORE_CERT_CN_INVALID. Consente un nome comune non valido in un certificato.</br>SECURITY_FLAG_IGNORE_CERT_DATE_INVALID. Consente una data di certificato non valida.</br>SECURITY_FLAG_IGNORE_UNKNOWN_CA. Consente un'autorità di certificazione non valida.</br>SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE. Consente di stabilire l'identità di un server con un certificato non server.</br>WINHTTP_ENABLE_SSL_REVOCATION. Consente la revoca SSL. Se questo flag è impostato, i flag precedenti verranno ignorati. |
| DODownloadProperty_CallbackFreqPercent | facoltativo. Usare questa proprietà per impostare o ottenere la frequenza di callback in base alla percentuale di download. Il tipo VARIANT è VT_UI4. |
| DODownloadProperty_CallbackFreqSeconds | facoltativo. Usare questa proprietà per impostare o ottenere la frequenza di callback in base al tempo di download. Il valore predefinito è ogni secondo. Il tipo VARIANT è VT_UI4. |
| DODownloadProperty_NoProgressTimeoutSeconds | facoltativo. Usare questa proprietà per impostare o ottenere la lunghezza del timeout di download per nessun avanzamento. Il valore minimo accettato è 60 secondi di nessuna attività di download. Il tipo VARIANT è VT_UI4. |
| DODownloadProperty_ForegroundPriority | facoltativo. Usare questa proprietà per impostare o ottenere la priorità di download corrente. VARIANT_TRUE valore porta il download in primo piano con priorità più alta. Il valore predefinito è la priorità in background. Il tipo VARIANT è VT_BOOL. |
| DODownloadProperty_BlockingMode | facoltativo. Usare questa proprietà per impostare o ottenere la modalità di blocco del download corrente. VARIANT_TRUE valore causerà il blocco **di IDODownload::Start** fino al completamento del download o al verificarsi di un errore. Il valore predefinito è la modalità non di blocco. Il tipo VARIANT è VT_BOOL. |
| DODownloadProperty_CallbackInterface | facoltativo. Usare questa proprietà per impostare o ottenere il puntatore **all'interfaccia IDODownloadStatusCallback usata** per i callback di download. Il tipo VARIANT è VT_UNKNOWN. |
| DODownloadProperty_StreamInterface | facoltativo. Usare questa proprietà per impostare o ottenere il puntatore all'interfaccia IStream usata per il tipo di download del flusso. Il tipo VARIANT è VT_UNKNOWN. |
| DODownloadProperty_SecurityContext | Facoltativo di sola scrittura. Utilizzare questa proprietà per impostare il contesto del certificato da utilizzare durante le operazioni di richiesta HTTP. Il valore deve essere costituito da byte serializzati di CERT_CONTEXT. Il tipo VARIANT è \| (VT_ARRAY VT_UI1). |
| DODownloadProperty_NetworkToken | Facoltativo di sola scrittura. Usare questa proprietà per impostare il token di rete da usare durante le operazioni HTTP. VARIANT_TRUE valore fa in modo che DO acquisisca il token di identità del chiamante e VARIANT_FALSE cancella il token esistente. Il valore predefinito è il token dell'utente connesso. Il tipo VARIANT è VT_BOOL. |
| DODownloadProperty_CorrelationVector | facoltativo. Imposta un vettore di correlazione specifico per scopi di telemetria. Il tipo VARIANT è VT_BSTR. |
| DODownloadProperty_DecryptionInfo | Facoltativo di sola scrittura. Imposta le informazioni di decrittografia sotto forma di stringa JSON. Il tipo VARIANT è VT_BSTR. |
| DODownloadProperty_IntegrityCheckInfo | Facoltativo di sola scrittura. Imposta il percorso del file hash della parte (PHF), usato da DO per eseguire i controlli di integrità di runtime sul contenuto scaricato. Il tipo VARIANT è VT_BSTR. |
| DODownloadProperty_IntegrityCheckMandatory | facoltativo. Imposta un flag booleano che indica se l'utilizzo del file hash della parte (PHF) è obbligatorio. Se VARIANT_TRUE, il download verrà interrotto se il controllo di integrità non riesce. Il tipo VARIANT è VT_BOOL. |
| DODownloadProperty_TotalSizeBytes | facoltativo. Specifica le dimensioni totali del download in byte. Il tipo VARIANT è VT_UI8. |

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, versione 1809 \[ Solo applicazioni Win32\] |
| **Intestazione** | DeliveryOptimizationDownloadTypes.h |
