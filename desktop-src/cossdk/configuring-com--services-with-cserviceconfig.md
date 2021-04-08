---
description: Configurazione dei servizi COM+ con CServiceConfig
ms.assetid: c44743a8-8b91-4e2a-9ba4-4cb6ae787999
title: Configurazione dei servizi COM+ con CServiceConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8bbc6c3131347f450340863db70fd9b3999730
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748050"
---
# <a name="configuring-com-services-with-cserviceconfig"></a>Configurazione dei servizi COM+ con CServiceConfig

La classe [**CServiceConfig**](cserviceconfig.md) viene utilizzata per configurare i servizi com+ che possono essere utilizzati senza componenti. Aggrega il gestore di marshalling a thread libero, in modo che possa essere usato in diversi Apartment. Per configurare un singolo servizio, è necessario chiamare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per l'interfaccia associata al servizio e quindi chiamare i metodi su tale interfaccia per stabilire la configurazione appropriata. Nella tabella seguente vengono descritte le interfacce implementate tramite la classe **CServiceConfig** .



| Interfaccia                                                                         | Descrizione                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IServiceInheritanceConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/>         | Interfaccia predefinita per la classe. Viene usato per inizializzare rapidamente molti dei servizi COM+.<br/>                                                                                              |
| [**IServiceComTIIntrinsicsConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> | Utilizzato per configurare le informazioni intrinseche COM Transaction Integrator (COMTI). COMTI consente agli sviluppatori di integrare programmi di transazione basati su mainframe con applicazioni basate su componenti.<br/> |
| [**IServiceIISIntrinsicsConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/>     | Utilizzato per configurare le informazioni intrinseche di Internet Information Services (IIS).<br/>                                                                                                             |
| [**IServicePartitionConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/>             | Utilizzato per configurare la modalità di utilizzo delle partizioni COM+ con i servizi.<br/>                                                                                                                             |
| [**IServiceSxSConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/>                         | Utilizzato per configurare gli assembly affiancati.<br/>                                                                                                                                                    |
| [**IServiceSynchronizationConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> | Utilizzato per configurare i servizi di sincronizzazione COM+.<br/>                                                                                                                                              |
| [**IServiceThreadPoolConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/>           | Utilizzato per configurare il pool di thread per il servizio COM+. Il pool di thread può essere configurato solo quando si usa la funzione [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) .<br/>                          |
| [**IServiceTrackerConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/>                 | Utilizzato per configurare la proprietà Tracker. Tracker è un meccanismo di creazione di report utilizzato dal codice di monitoraggio per controllare quale codice viene eseguito quando.<br/>                                                         |
| [**IServiceTransactionConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/>         | Utilizzato per configurare il servizio di transazione COM+.<br/>                                                                                                                                               |



 

## <a name="component-services-administrative-tool"></a>Strumento di amministrazione Servizi componenti

Non è valida.

## <a name="visual-basic"></a>Visual Basic

Non è valida.

## <a name="cc"></a>C/C++

Nel frammento di codice seguente viene illustrato come creare e configurare un oggetto [**CServiceConfig**](cserviceconfig.md) per l'utilizzo di transazioni com+.


```C++
// Create a CServiceConfig object.
HRESULT hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
  IID_IUnknown, (void**)&pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Query for the IServiceInheritanceConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceInheritanceConfig, 
  (void**)&pInheritanceConfig);
if (FAILED(hr)) throw(hr);

// Inherit the current context before using transactions.
hr = pInheritanceConfig->ContainingContextTreatment(CSC_Inherit);
if (FAILED(hr)) throw(hr);

// Query for the IServiceTransactionConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceTransactionConfig, 
  (void**)&pTransactionConfig);
if (FAILED(hr)) throw(hr);

// Configure transactions to always create a new one.
hr = pTransactionConfig->ConfigureTransaction(CSC_NewTransaction);
if (FAILED(hr)) throw(hr);

// Set the isolation level of the transactions to ReadCommitted.
hr = pTransactionConfig->IsolationLevel( 
  COMAdminTxIsolationLevelReadCommitted);
if (FAILED(hr)) throw(hr);

// Set the transaction time-out to 1 minute.
hr = pTransactionConfig->TransactionTimeout(60);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CServiceConfig**](cserviceconfig.md)
</dt> <dt>

[Uso dei servizi COM+ tramite CoCreateActivity](using-com--services-through-cocreateactivity.md)
</dt> <dt>

[Uso dei servizi COM+ tramite CoEnterServiceDomain e CoLeaveServiceDomain](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

